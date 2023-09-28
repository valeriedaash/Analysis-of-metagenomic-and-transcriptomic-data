genome_sequence = input()

start_codon = "ATG"
stop_codons = ['TAA', 'TGA', 'TAG']

index = 0

while index < len(genome_sequence):
    for i in stop_codons:
        start_index = genome_sequence.find(start_codon, index)
    
        if start_index == -1:
            break
        
        stop_index = genome_sequence.find(i, start_index)
    
        if stop_index == -1:
            break
                
        reading_frame = genome_sequence[start_index:stop_index + 3]
        
        if len(reading_frame) % 3 == 0 and len(reading_frame) >= 15:
            print(f"Начало считывания с индекса {start_index}, Конец считывания с индекса {stop_index}: {reading_frame}")
        index = stop_index + 4
        # Начинаем поиск следующей рамки считывания после стоп-кодона
    index = stop_index + 4
