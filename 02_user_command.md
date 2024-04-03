In Slurm, user-related commands allow administrators and users to manage user accounts,
permissions, and resource allocation within the cluster. 
Here's an overview of common user-related commands in Slurm, along with examples:

### 1. `sacctmgr`:
This command is used for managing Slurm accounts, users, associations, and configurations.

**Syntax for adding a new user:**
```bash
sudo sacctmgr add user username
```

**Example:**
```bash
sudo sacctmgr add user john
```

### 2. `sacct`:
This command is used to display job accounting information, including job status, start time, end time, and resource usage.

**Syntax:**
```bash
sacct [options]
```

**Example:**
```bash
sacct -u john
```

### 3. `squeue`:
This command is used to display the status of jobs in the queue, including the user who submitted the jobs.

**Syntax:**
```bash
squeue [options]
```

**Example:**
```bash
squeue -u john
```

### 4. `sinfo`:
This command is used to display information about partitions, nodes, and node states in the cluster.

**Syntax:**
```bash
sinfo [options]
```

**Example:**
```bash
sinfo -Nl
```

### 5. `scontrol`:
This command is used to view and modify Slurm configuration and state.

**Syntax for setting user associations:**
```bash
sudo scontrol update user where name=username set account=accountname
```

**Example:**
```bash
sudo scontrol update user where name=john set account=projectA
```

### 6. `scancel`:
This command is used to cancel or terminate jobs submitted by users.

**Syntax:**
```bash
scancel job_id
```

**Example:**
```bash
scancel 12345
```

### 7. `sreport`:
This command is used to generate various reports based on Slurm job and accounting data.

**Syntax for generating user-specific reports:**
```bash
sreport user topusers
```

**Example:**
```bash
sreport user topusers start=2022-01-01 end=2022-01-31
```

Sure, here are some common user-related commands in Slurm along with their explanations and examples:

### 8. `sbatch`:
- **Explanation:** This command is used to submit a batch script for execution on the cluster.
- **Syntax:**
  ```bash
  sbatch [options] batch_script
  ```
- **Example:**
  ```bash
  sbatch my_job_script.sh
  ```


These are some of the common user-related commands in Slurm. 
They provide administrators and users with the tools necessary to manage job submission, monitor job status, and allocate resources effectively within the cluster.
Always consult the Slurm documentation or command manuals for more options and detailed usage instructions.
