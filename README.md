<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meghalaya Job Alert</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 0; padding: 0; background-color: #f4f4f4; }
        header { background-color: #007bff; color: white; text-align: center; padding: 20px; }
        .container { max-width: 1200px; margin: 20px auto; padding: 20px; background: white; border-radius: 8px; box-shadow: 0 0 10px rgba(0,0,0,0.1); }
        .job-list { list-style: none; padding: 0; }
        .job-item { border-bottom: 1px solid #ddd; padding: 15px; margin-bottom: 10px; }
        .job-item h3 { margin: 0; color: #333; }
        .job-item p { margin: 5px 0; }
        .filter { margin-bottom: 20px; }
        .filter input { padding: 10px; width: 100%; max-width: 300px; }
        footer { text-align: center; padding: 10px; background: #007bff; color: white; margin-top: 20px; }
    </style>
</head>
<body>
    <header>
        <h1>Meghalaya Job Alert</h1>
        <p>Stay updated with the latest job opportunities in Meghalaya, India.</p>
    </header>
    
    <div class="container">
        <div class="filter">
            <input type="text" id="search" placeholder="Search jobs by title or location...">
        </div>
        <ul class="job-list" id="jobList">
            <!-- Placeholder job listings -->
            <li class="job-item">
                <h3>Software Developer</h3>
                <p><strong>Location:</strong> Shillong, Meghalaya</p>
                <p><strong>Company:</strong> Tech Solutions Ltd.</p>
                <p><strong>Description:</strong> Develop web applications. Experience in JavaScript required.</p>
                <p><strong>Apply:</strong> <a href="mailto:jobs@techsolutions.com">jobs@techsolutions.com</a></p>
            </li>
            <li class="job-item">
                <h3>Teacher</h3>
                <p><strong>Location:</strong> Tura, Meghalaya</p>
                <p><strong>Company:</strong> Meghalaya Education Board</p>
                <p><strong>Description:</strong> Teach secondary school students. B.Ed required.</p>
                <p><strong>Apply:</strong> <a href="https://meghalaya.gov.in/jobs">Apply Online</a></p>
            </li>
            <li class="job-item">
                <h3>Nurse</h3>
                <p><strong>Location:</strong> Jowai, Meghalaya</p>
                <p><strong>Company:</strong> Civil Hospital</p>
                <p><strong>Description:</strong> Provide patient care. Nursing diploma essential.</p>
                <p><strong>Apply:</strong> <a href="mailto:hr@civilhospital.megh">hr@civilhospital.megh</a></p>
            </li>
            <!-- Add more jobs here -->
        </ul>
    </div>
    
    <footer>
        <p>&copy; 2023 Meghalaya Job Alert. For real-time updates, subscribe to our newsletter.</p>
    </footer>
    
    <script>
        const searchInput = document.getElementById('search');
        const jobList = document.getElementById('jobList');
        const jobs = jobList.getElementsByClassName('job-item');
        
        searchInput.addEventListener('input', function() {
            const query = this.value.toLowerCase();
            Array.from(jobs).forEach(job => {
                const text = job.textContent.toLowerCase();
                job.style.display = text.includes(query) ? '' : 'none';
            });
        });
    </script>
</body>
</html>
