---
title: Installation des procédures d’e/s personnalisées
description: Installation des procédures d’e/s personnalisées
ms.assetid: 7b26a062-fa52-4de3-b8c8-b9f9167068fc
keywords:
- e/s de fichier multimédia, procédures personnalisées
- e/s de fichier, procédures personnalisées
- entrées et sorties (e/s), procédures personnalisées
- E/s (entrée et sortie), procédures personnalisées
- installation des procédures d’e/s personnalisées
- e/s personnalisées
- mmioInstallIOProc fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1574b7076e7344fa8e800ef1f18ad13fcfd3f3af
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381946"
---
# <a name="installing-custom-io-procedures"></a><span data-ttu-id="fa836-110">Installation des procédures d’e/s personnalisées</span><span class="sxs-lookup"><span data-stu-id="fa836-110">Installing Custom I/O Procedures</span></span>

<span data-ttu-id="fa836-111">Pour installer une procédure d’e/s associée au. L’extension de nom de fichier ARC, utilisez la fonction [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) comme suit :</span><span class="sxs-lookup"><span data-stu-id="fa836-111">To install an I/O procedure associated with the .ARC filename extension, use the [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) function as follows:</span></span>


```C++
mmioInstallIOProc (mmioFOURCC('A', 'R', 'C', ' '), 
    (LPMMIOPROC)lpmmioproc, MMIO_INSTALLPROC); 
```



<span data-ttu-id="fa836-112">Lorsque vous installez une procédure d’e/s à l’aide de [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc), la procédure reste installée jusqu’à ce que vous la supprimiez.</span><span class="sxs-lookup"><span data-stu-id="fa836-112">When you install an I/O procedure using [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc), the procedure remains installed until you remove it.</span></span> <span data-ttu-id="fa836-113">La procédure d’e/s est utilisée pour tout fichier que vous ouvrez tant que le fichier a l’extension de nom de fichier appropriée.</span><span class="sxs-lookup"><span data-stu-id="fa836-113">The I/O procedure is used for any file you open as long as the file has the appropriate filename extension.</span></span>

<span data-ttu-id="fa836-114">Vous pouvez également installer temporairement une procédure d’e/s à l’aide de la fonction [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) .</span><span class="sxs-lookup"><span data-stu-id="fa836-114">You can also temporarily install an I/O procedure by using the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span> <span data-ttu-id="fa836-115">Dans ce cas, la procédure d’e/s est utilisée uniquement avec un fichier ouvert à l’aide de **mmioOpen** et elle est supprimée lorsque le fichier est fermé à l’aide de la fonction [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) .</span><span class="sxs-lookup"><span data-stu-id="fa836-115">In this case, the I/O procedure is used only with a file opened by using **mmioOpen** and is removed when the file is closed by using the [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) function.</span></span> <span data-ttu-id="fa836-116">Pour spécifier une procédure d’e/s lorsque vous ouvrez un fichier à l’aide de **mmioOpen**, utilisez le paramètre *lpmmioinfo* pour référencer une structure [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) comme suit :</span><span class="sxs-lookup"><span data-stu-id="fa836-116">To specify an I/O procedure when you open a file by using **mmioOpen**, use the *lpmmioinfo* parameter to reference an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure as follows:</span></span>

1.  <span data-ttu-id="fa836-117">Affectez la valeur **null** au membre **fccIOProc** .</span><span class="sxs-lookup"><span data-stu-id="fa836-117">Set the **fccIOProc** member to **NULL**.</span></span>
2.  <span data-ttu-id="fa836-118">Définissez le membre **pIOProc** sur l’adresse de l’instance de procédure de la procédure d’e/s.</span><span class="sxs-lookup"><span data-stu-id="fa836-118">Set the **pIOProc** member to the procedure-instance address of the I/O procedure.</span></span>
3.  <span data-ttu-id="fa836-119">Affectez à tous les autres membres la valeur zéro (sauf si vous ouvrez un fichier de mémoire ou si vous lisez ou écrivez directement dans le tampon d’e/s de fichier).</span><span class="sxs-lookup"><span data-stu-id="fa836-119">Set all other members to zero (unless you are opening a memory file, or directly reading or writing to the file I/O buffer).</span></span>

<span data-ttu-id="fa836-120">Veillez à supprimer toutes les procédures d’e/s que vous avez installées avant de quitter votre application.</span><span class="sxs-lookup"><span data-stu-id="fa836-120">Be sure to remove any I/O procedures you have installed before you exit your application.</span></span>

 

 