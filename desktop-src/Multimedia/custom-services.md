---
title: Services personnalisés
description: Services personnalisés
ms.assetid: 98b68205-3a34-4406-84de-bf2c8a5ed5b0
keywords:
- e/s de fichier multimédia, services personnalisés
- e/s de fichier, services personnalisés
- entrée et sortie (e/s), services personnalisés
- E/s (entrée et sortie), services personnalisés
- e/s personnalisées
- mmioInstallIOProc fonction)
- mmioOpen fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e41e3c5974fee9903c0864b1cfefccc8354b26a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031193"
---
# <a name="custom-services"></a><span data-ttu-id="bcf0a-110">Services personnalisés</span><span class="sxs-lookup"><span data-stu-id="bcf0a-110">Custom Services</span></span>

<span data-ttu-id="bcf0a-111">Les services d’e/s de fichier multimédia utilisent des procédures d’e/s pour gérer l’entrée et la sortie physiques associées à la lecture et l’écriture dans différents types de systèmes de stockage, tels que les systèmes d’archivage de fichiers et les systèmes de stockage de bases de données.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-111">Multimedia file I/O services use I/O procedures to handle the physical input and output associated with reading and writing to different types of storage systems, such as file-archival systems and database-storage systems.</span></span> <span data-ttu-id="bcf0a-112">Des procédures d’e/s prédéfinies existent pour les systèmes de fichiers standard et pour les fichiers de mémoire, mais vous pouvez fournir une procédure d’e/s personnalisée pour accéder à un système de stockage unique à l’aide de la fonction [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) .</span><span class="sxs-lookup"><span data-stu-id="bcf0a-112">Predefined I/O procedures exist for the standard file systems and for memory files, but you can supply a custom I/O procedure for accessing a unique storage system by using the [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) function.</span></span>

<span data-ttu-id="bcf0a-113">Pour ouvrir un fichier à l’aide d’une procédure d’e/s personnalisée, utilisez la fonction [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) .</span><span class="sxs-lookup"><span data-stu-id="bcf0a-113">To open a file by using a custom I/O procedure, use the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span> <span data-ttu-id="bcf0a-114">Incluez un signe plus (+) ou la constante CFSEPCHAR dans le nom de fichier pour séparer le nom du fichier physique du nom de l’élément du fichier que vous souhaitez ouvrir.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-114">Include a plus sign (+) or the CFSEPCHAR constant in the filename to separate the name of the physical file from the name of the element of the file you want to open.</span></span> <span data-ttu-id="bcf0a-115">L’exemple suivant ouvre un élément file nommé « element » à partir d’un fichier nommé FILENAME. ARC</span><span class="sxs-lookup"><span data-stu-id="bcf0a-115">The following example opens a file element named "element" from a file named FILENAME.ARC:</span></span>


```C++
mmioOpen("filename.arc+element", NULL, MMIO_READ); 
```



<span data-ttu-id="bcf0a-116">Lorsque le gestionnaire d’e/s de fichier rencontre un signe plus dans un nom de fichier, il examine l’extension de nom de fichier pour déterminer la procédure d’e/s à associer au fichier.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-116">When the file I/O manager encounters a plus sign in a filename, it examines the filename extension to determine which I/O procedure to associate with the file.</span></span> <span data-ttu-id="bcf0a-117">Dans l’exemple précédent, le gestionnaire d’e/s de fichier tenterait d’utiliser la procédure d’e/s associée au. Extension de nom de fichier ARC ; Cette procédure d’e/s aurait été installée à l’aide de [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc).</span><span class="sxs-lookup"><span data-stu-id="bcf0a-117">In the previous example, the file I/O manager would attempt to use the I/O procedure associated with the .ARC filename extension; this I/O procedure would have been installed by using [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc).</span></span> <span data-ttu-id="bcf0a-118">Si aucune procédure d’e/s n’est installée, [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-118">If no I/O procedure is installed, [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) returns an error.</span></span>

<span data-ttu-id="bcf0a-119">Les procédures d’e/s doivent répondre aux messages suivants :</span><span class="sxs-lookup"><span data-stu-id="bcf0a-119">I/O procedures must respond to the following messages:</span></span>

-   [<span data-ttu-id="bcf0a-120">**MMIOM \_ Fermer**</span><span class="sxs-lookup"><span data-stu-id="bcf0a-120">**MMIOM\_CLOSE**</span></span>](mmiom-close.md)
-   [<span data-ttu-id="bcf0a-121">**MMIOM \_ ouvrir**</span><span class="sxs-lookup"><span data-stu-id="bcf0a-121">**MMIOM\_OPEN**</span></span>](mmiom-open.md)
-   [<span data-ttu-id="bcf0a-122">**\_lecture MMIOM**</span><span class="sxs-lookup"><span data-stu-id="bcf0a-122">**MMIOM\_READ**</span></span>](mmiom-read.md)
-   [<span data-ttu-id="bcf0a-123">**\_écriture MMIOM**</span><span class="sxs-lookup"><span data-stu-id="bcf0a-123">**MMIOM\_WRITE**</span></span>](mmiom-write.md)
-   [<span data-ttu-id="bcf0a-124">**MMIOM \_ Seek**</span><span class="sxs-lookup"><span data-stu-id="bcf0a-124">**MMIOM\_SEEK**</span></span>](mmiom-seek.md)
-   [<span data-ttu-id="bcf0a-125">**MMIOM \_ REnommer**</span><span class="sxs-lookup"><span data-stu-id="bcf0a-125">**MMIOM\_RENAME**</span></span>](mmiom-rename.md)
-   [<span data-ttu-id="bcf0a-126">**MMIOM \_ WRITEFLUSH**</span><span class="sxs-lookup"><span data-stu-id="bcf0a-126">**MMIOM\_WRITEFLUSH**</span></span>](mmiom-writeflush.md)

<span data-ttu-id="bcf0a-127">Vous pouvez également créer des messages personnalisés et les envoyer à votre procédure d’e/s à l’aide de la fonction [**mmioSendMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage) .</span><span class="sxs-lookup"><span data-stu-id="bcf0a-127">You can also create custom messages and send them to your I/O procedure by using the [**mmioSendMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage) function.</span></span> <span data-ttu-id="bcf0a-128">Si vous définissez vos propres messages, assurez-vous qu’ils sont définis au niveau ou au-dessus de la valeur définie par la \_ constante utilisateur MMIOM.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-128">If you define your own messages, make sure they are defined at or above the value defined by the MMIOM\_USER constant.</span></span>

<span data-ttu-id="bcf0a-129">Outre le traitement des messages, une procédure d’e/s doit conserver le membre **lDiskOffset** de la structure [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) (pointée par le paramètre *lpmmioinfo* de la fonction **mmioOpen** ).</span><span class="sxs-lookup"><span data-stu-id="bcf0a-129">In addition to processing messages, an I/O procedure must maintain the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure (pointed to by the *lpmmioinfo* parameter of the **mmioOpen** function).</span></span> <span data-ttu-id="bcf0a-130">Le membre **lDiskOffset** doit toujours contenir le décalage de fichier à l’emplacement auquel le prochain \_ message d’écriture de MMIOM ou de lecture MMIOM \_ accédera.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-130">The **lDiskOffset** member must always contain the file offset to the location that the next MMIOM\_READ or MMIOM\_WRITE message will access.</span></span> <span data-ttu-id="bcf0a-131">L’offset est spécifié en octets et est relatif au début du fichier.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-131">The offset is specified in bytes and is relative to the beginning of the file.</span></span> <span data-ttu-id="bcf0a-132">La procédure d’e/s peut utiliser le membre **adwInfo** pour conserver les informations d’État requises.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-132">The I/O procedure can use the **adwInfo** member to maintain any required state information.</span></span> <span data-ttu-id="bcf0a-133">La procédure d’e/s ne doit pas modifier les autres membres de la structure **MMIOINFO** .</span><span class="sxs-lookup"><span data-stu-id="bcf0a-133">The I/O procedure should not modify any other members in the **MMIOINFO** structure.</span></span>

 

 