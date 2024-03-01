# mindmap.yml
Logarithm: #  inverse of exponentials

  Definition: #
    - Logarithm function # $y = log(x, b)$ <==> b^y = x
    - example 1 # log(8, 2) = 3 because 2^3 = 8
    - example 2 # log(27, 3) = 3 because 3^3 = 27
    
  Types:
    - Common logarithm  # log(x, 10)
    - Natural logarithm # log(x, e), log(x)
    
  Identities:
    - logarithm of 1 to any base   # log(1, b) = 0,   (b ≠ 1)
    - logarithm of the base itself # log(b, b) = 1,   (b > 0)
    - inverse of exponentiation    # b^log(x, b) = x, (b > 0)
  
  Manipulations:
    - product rule    # log(m * n, b) <==> log(m, b) + log(n, b)
    - quotient rule   # log(m/n, b)   <==> log(m, b) - log(n, b)
    - reciprocal rule # log(1/x, b)   <==> - log(x, b)
    - power rule      # log(m^n, b)   <==> n * log(m, b)
    - change of base  # log(x, a)     <==> log(x, b) / log(a, b)
