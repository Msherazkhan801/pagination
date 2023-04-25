# pagination
const [currentPage, setCurrentPage] = useState(1);
   const [postsPerPage] = useState(3);
   const indexOfLastPost = currentPage * postsPerPage;
   const indexOfFirstPost = indexOfLastPost - postsPerPage;
   const currentPosts = blogPosts.slice(indexOfFirstPost, indexOfLastPost);
import React from 'react';
 ####make a component
const Paginate = ({ postsPerPage, totalPosts }) => {
   const pageNumbers = [];
 
   for (let i = 1; i <= Math.ceil(totalPosts / postsPerPage); i++) {
      pageNumbers.push(i);
   }
 
   return (
      <div className="pagination-container">
         <ul className="pagination">
            {pageNumbers.map((number) => (
               <li key={number} className="page-number">
                  {number}
               </li>
            ))}
         </ul>
      </div>
   );
};
 
export default Paginate;


################################
sort#
const sortedData = data.sort((a, b) => new Date(a.date) - new Date(b.date));
