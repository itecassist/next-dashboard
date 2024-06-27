https://nextjs.org/learn/dashboard-app

Using the clsx library to toggle class names
There may be cases where you may need to conditionally style an element based on state or some other condition.
clsx is a library that lets you toggle class names easily. We recommend taking a look at documentation
for more details, but here's the basic usage:
    Suppose that you want to create an InvoiceStatus component which accepts status. The status can be 'pending' or 'paid'.
    If it's 'paid', you want the color to be green. If it's 'pending', you want the color to be gray.

import clsx from 'clsx';

export default function InvoiceStatus({ status }: { status: string }) {
  return (
    <span
      className={clsx(
        'inline-flex items-center rounded-full px-2 py-1 text-sm',
        {
          'bg-gray-100 text-gray-500': status === 'pending',
          'bg-green-500 text-white': status === 'paid',
        },
      )}
    >
    // ...
)}