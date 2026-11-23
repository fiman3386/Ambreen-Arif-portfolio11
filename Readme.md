import streamlit as st

st.set_page_config(
    page_title="Ambreen Arif | Portfolio",
    page_icon="🎓",
    layout="wide"
)

# Dark theme styling
st.markdown("""
<style>
.stApp {
    background-color: #101827;
    color: #F8FAFC;
}

section[data-testid="stSidebar"] {
    background-color: #172235;
}

h1, h2, h3 {
    color: #A5B4FC !important;
}

p, label {
    color: #E2E8F0;
}

div[data-testid="stMetric"] {
    background-color: #1E293B;
    padding: 18px;
    border-radius: 12px;
    border: 1px solid #334155;
}

a {
    color: #A5B4FC !important;
}
</style>
""", unsafe_allow_html=True)

# Personal information
NAME = "Ambreen Arif"
DEGREE = "BS Mathematics"
UNIVERSITY = "Bahauddin Zakariya University (BZU), Multan"
DEPARTMENT = "CASPAM"
LOCATION = "Multan, Pakistan"

LINKEDIN = "https://lnkd.in/p/dq6Dcg_Z"
GITHUB = "https://github.com/fiman3386/Ambreen-Arif-Academic-Portfolio"

# Sidebar
with st.sidebar:
    st.title("🎓 Ambreen Arif")
    st.caption("Academic Portfolio")
    page = st.radio(
        "Navigation",
        ["Home", "About Me", "Education", "Skills",
         "Projects", "Achievements", "Contact"]
    )

    st.divider()
    st.markdown(f"[LinkedIn]({LINKEDIN})")
    st.markdown(f"[GitHub]({GITHUB})")

# Home
if page == "Home":
    st.title("Hello, I'm Ambreen Arif 👋")
    st.subheader("Mathematics Student | Python | Machine Learning")
    st.write("Welcome to my academic and professional portfolio.")
    st.write(
        "I am interested in mathematics, programming, "
        "data analysis and artificial intelligence."
    )

    col1, col2, col3 = st.columns(3)
    col1.metric("Degree", "BS Mathematics")
    col2.metric("University", "BZU Multan")
    col3.metric("Department", "CASPAM")

    st.divider()
    st.header("My Academic Journey")
    st.write("Combining mathematical knowledge with modern technology.")

# About
elif page == "About Me":
    st.title("About Me")
    st.write(
        "I am a BS Mathematics student at Bahauddin Zakariya "
        "University, Multan. I am interested in Python, "
        "machine learning, data analysis and mathematical modelling."
    )
    st.write("My goal is to apply mathematics and computational "
             "thinking to practical real-world problems.")

# Education
elif page == "Education":
    st.title("My Education")
    st.subheader(DEGREE)
    st.write(UNIVERSITY)
    st.write("Department:", DEPARTMENT)
    st.write("Location:", LOCATION)

# Skills
elif page == "Skills":
    st.title("Technical Skills")
    skills = [
        "Python Programming",
        "Machine Learning",
        "Data Analysis",
        "Mathematical Modelling",
        "Streamlit",
        "Graph Theory"
    ]
    for skill in skills:
        st.write("•", skill)

# Projects
elif page == "Projects":
    st.title("My Academic Projects")

    with st.container(border=True):
        st.subheader("FMCG Inventory Management System")
        st.write("Area: Machine Learning")
        st.write("Algorithm: Random Forest")
        st.write("Focus: Inventory management and risk analysis.")

    with st.container(border=True):
        st.subheader("SmartNotes AI")
        st.write("Area: Artificial Intelligence")
        st.write("Focus: Summarizing study notes and generating questions.")

    with st.container(border=True):
        st.subheader("MathMate AI")
        st.write("Area: RAG-Based Study Assistant")
        st.write("Focus: Helping students understand mathematics.")

# Achievements
elif page == "Achievements":
    st.title("Certificates & Achievements")
    st.write("Certificates, workshops and academic achievements "
             "can be added here.")

# Contact
elif page == "Contact":
    st.title("Connect With Me")
    st.markdown(f"[🔵 LinkedIn Profile]({LINKEDIN})")
    st.markdown(f"[💻 GitHub Profile]({GITHUB})")
    st.write("Location:", LOCATION)

st.divider()
st.caption("© 2026 Ambreen Arif | Academic Portfolio")
