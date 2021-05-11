# Skelibras - provisional website
Skelibras: a large annotated skeleton dataset of dynamic Libras signs comprised of unsegmented and segmented conversations.

# Dataset organiztion
- Sign Name
    - VideoID---SignName---BeginInMiliseconds---EndInMiliSeconds---View---SignalyID.csv

All CSVs have the keys corresponding to the extracted joints, hand and body. All indices correspond to frames. And each joint is a string from a numpy.array, which can be mapped back to numpy.array as follows: 

```python
def parse_npy_vec_str(str_array_like):
    if not isinstance(str_array_like, str):
        return str_array_like

    res = str_array_like[1:len(str_array_like) - 1].split(' ')
    recovered_np_array = []
    for r in res:
        if r == '' or ' ' in r:
            continue
        f = float(r)
        recovered_np_array.append(f)
    return np.array(recovered_np_array)
        
sign = sign.applymap(parse_npy_vec_str)

```

# Downloads link:
[Skelibras download part 1](https://drive.google.com/file/d/1VlbKdWDIHHIvOA5_qRtp5OoBZQ9t4zPC/view?usp=sharing)

[Skelibras download part 2](https://drive.google.com/file/d/49dcd91231f801159e893fb5c6674985/view?usp=sharing)

[Skelibras download part 3]()

[Skelibras download part 4]()

[Skelibras download part 5]()


# Cite us
