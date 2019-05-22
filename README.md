# labs-TV
def permute(A):
    if len(A)==1:
        return [tuple(A)]
    permutations = []
    for x in A:
        for y in permute(A-{x}):
            permutations.append((x,)+y)
    return permutations
A = {1, 3, 5}
permute_all = set(permute(A))
print("Перестановки множини {}: {}".format(A,permute_all))
print("Кількість перестановок: ", len(permute_all))
