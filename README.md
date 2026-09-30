# IST-230
Discrete Mathematics 
def negation(p: bool) -> bool:
    """
    Returns the logical negation of p (¬p).
    """
    return not p

def conjunction(p: bool, q: bool) -> bool:
    """
    Returns the logical conjunction of p and q (p ∧ q).
    """
    # TODO:
    return p and q

def disjunction(p: bool, q: bool) -> bool:
    """
    Returns the logical disjunction of p and q (p ∨ q).
    """
    # TODO: 
    return p or q

def exclusive_or(p: bool, q: bool) -> bool:
    """
    Returns the exclusive OR of p and q (p ⊕ q).
    Evaluates to True if exactly one of the inputs is True.
    """
    # TODO: 
    return (p and not q) or (not p and q)


    # ==========================================
# ZYBOOKS SECTION 1.3: CONDITIONAL OPERATIONS
# ==========================================

def conditional(p: bool, q: bool) -> bool:
    """
    Returns the implication p → q.
    Remember the rule from Section 1.3: This is False ONLY when 
    the hypothesis (p) is True and the conclusion (q) is False.
    """
    # TODO: 
    return (not p or to q)

def biconditional(p: bool, q: bool) -> bool:
    """
    Returns the biconditional evaluation of p and q (p ↔ q).
    """
    # TODO: 
    return p==q


# ==========================================
# AUTOMATED TRUTH TABLE GENERATOR
# ==========================================

def run_truth_table_generator():
    """
    Loops through all 4 structural binary truth assignments 
    and displays the completed evaluations.
    """
    print(f"{'p':<6} | {'q':<6} | {'¬p':<6} | {'p ∧ q':<6} | {'p → q':<12} | {'q → p (Conv)':<13}")
    print("-" * 60)
    
    # Truth matrix combinations
    combinations = [(True, True), (True, False), (False, True), (False, False)
    
    for p, q in combinations:
        try:
            # These will evaluate correctly once students fill in the blocks above
            not_p = negation(p)
            and_op = conjunction(p, q)
            imp_op = conditional(p, q)
            conv_op = conditional(q, p) # Converse logic
            
            print(f"{str(p):<6} | {str(q):<6} | {str(not_p):<6} | {str(and_op):<6} | {str(imp_op):<12} | {str(conv_op):<13}")
        except Exception:
            print(f"{str(p):<6} | {str(q):<6} | [Functions Not Implemented Yet]")

if __name__ == "__main__":
    print("IST 230 Lab - Chapter 1 Evaluation Matrix")
    run_truth_table_generator()