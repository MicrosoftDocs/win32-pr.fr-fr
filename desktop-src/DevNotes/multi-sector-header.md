---
description: Représente l’en-tête multisecteur.
ms.assetid: 0fad0e93-b940-4b52-be16-c5f177884dfb
title: Structure MULTI_SECTOR_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MULTI_SECTOR_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: ab21e17b83ae25286d2775d9dbd97dfd4cf493bc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747884"
---
# <a name="multi_sector_header-structure"></a><span data-ttu-id="84c06-103">\_Structure d' \_ en-tête multisecteur</span><span class="sxs-lookup"><span data-stu-id="84c06-103">MULTI\_SECTOR\_HEADER structure</span></span>

<span data-ttu-id="84c06-104">\[Cette structure est valide uniquement pour la version 3 des volumes NTFS ; elles peuvent être modifiées dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="84c06-104">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="84c06-105">Représente l’en-tête multisecteur.</span><span class="sxs-lookup"><span data-stu-id="84c06-105">Represents the multisector header.</span></span>

## <a name="syntax"></a><span data-ttu-id="84c06-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84c06-106">Syntax</span></span>


```C++
typedef struct _MULTI_SECTOR_HEADER {
  UCHAR  Signature[4];
  USHORT UpdateSequenceArrayOffset;
  USHORT UpdateSequenceArraySize;
} MULTI_SECTOR_HEADER, *PMULTI_SECTOR_HEADER;
```



## <a name="members"></a><span data-ttu-id="84c06-107">Membres</span><span class="sxs-lookup"><span data-stu-id="84c06-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="84c06-108">**Signature**</span><span class="sxs-lookup"><span data-stu-id="84c06-108">**Signature**</span></span>
</dt> <dd>

<span data-ttu-id="84c06-109">Signature.</span><span class="sxs-lookup"><span data-stu-id="84c06-109">The signature.</span></span> <span data-ttu-id="84c06-110">Cette valeur est une pratique pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="84c06-110">This value is a convenience to the user.</span></span>

</dd> <dt>

<span data-ttu-id="84c06-111">**UpdateSequenceArrayOffset**</span><span class="sxs-lookup"><span data-stu-id="84c06-111">**UpdateSequenceArrayOffset**</span></span>
</dt> <dd>

<span data-ttu-id="84c06-112">Offset du tableau de séquence de mise à jour, à partir du début de cette structure.</span><span class="sxs-lookup"><span data-stu-id="84c06-112">The offset to the update sequence array, from the start of this structure.</span></span> <span data-ttu-id="84c06-113">Le tableau de séquence de mise à jour doit se terminer avant la dernière valeur USHORT dans le premier secteur.</span><span class="sxs-lookup"><span data-stu-id="84c06-113">The update sequence array must end before the last USHORT value in the first sector.</span></span>

</dd> <dt>

<span data-ttu-id="84c06-114">**UpdateSequenceArraySize**</span><span class="sxs-lookup"><span data-stu-id="84c06-114">**UpdateSequenceArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="84c06-115">Taille du tableau de séquences de mise à jour, en octets.</span><span class="sxs-lookup"><span data-stu-id="84c06-115">The size of the update sequence array, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84c06-116">Notes</span><span class="sxs-lookup"><span data-stu-id="84c06-116">Remarks</span></span>

<span data-ttu-id="84c06-117">Notez qu’il n’y a aucun fichier d’en-tête associé pour cette structure.</span><span class="sxs-lookup"><span data-stu-id="84c06-117">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="84c06-118">Cette définition de structure est valide uniquement pour la version majeure de la version 3 et la version mineure 0 ou 1, comme indiqué par [**FSCTL \_ obtenir les \_ \_ \_ données du volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="84c06-118">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="84c06-119">L’en-tête multisecteur et le tableau de séquence de mise à jour assurent la détection de transferts multisectoriels incomplets pour les appareils qui ont une taille de secteur physique supérieure ou égale au Stride du numéro de séquence (512) ou qui ne transfèrent pas les secteurs dans le désordre.</span><span class="sxs-lookup"><span data-stu-id="84c06-119">The multisector header and update sequence array provide detection of incomplete multisector transfers for devices that either have a physical sector size greater than or equal to the sequence number stride (512) or that do not transfer sectors out of order.</span></span> <span data-ttu-id="84c06-120">Si un appareil dont la taille des secteurs est inférieure au Stride du numéro de séquence et qu’il transfère parfois des secteurs dans le désordre, le tableau de séquences de mise à jour ne fournit pas de détection absolue des transferts incomplets.</span><span class="sxs-lookup"><span data-stu-id="84c06-120">If a device exists that has a sector size smaller than the sequence number stride and it sometimes transfers sectors out of order, then the update sequence array will not provide absolute detection of incomplete transfers.</span></span> <span data-ttu-id="84c06-121">Le nombre de séquences Stride est défini sur un nombre suffisamment petit pour fournir une protection absolue pour tous les disques durs connus.</span><span class="sxs-lookup"><span data-stu-id="84c06-121">The sequence number stride is set to a small enough number to provide absolute protection for all known hard disks.</span></span> <span data-ttu-id="84c06-122">Il n’est pas défini sur une taille inférieure ou il peut y avoir un temps d’exécution excessif ou une surcharge d’espace.</span><span class="sxs-lookup"><span data-stu-id="84c06-122">It is not set any smaller or there might be excessive run time or space overhead.</span></span>

<span data-ttu-id="84c06-123">Le tableau de séquences de mise à jour se compose d’un tableau de *n* valeurs **UShort** , où *n* est la taille de la structure protégée divisée par le numéro de séquence Stride.</span><span class="sxs-lookup"><span data-stu-id="84c06-123">The update sequence array consists of an array of *n* **USHORT** values, where *n* is the size of the structure being protected divided by the sequence number stride.</span></span> <span data-ttu-id="84c06-124">Le premier mot contient le numéro de séquence de mise à jour, qui est un compteur cyclique du nombre de fois où la structure conteneur a été écrite sur le disque.</span><span class="sxs-lookup"><span data-stu-id="84c06-124">The first word contains the update sequence number, which is a cyclical counter of the number of times the containing structure has been written to disk.</span></span> <span data-ttu-id="84c06-125">Les *n* valeurs **UShort** enregistrées sont ensuite remplacées par le numéro de séquence de mise à jour lors de la dernière écriture sur le disque de la structure conteneur.</span><span class="sxs-lookup"><span data-stu-id="84c06-125">Next are the *n* saved **USHORT** values that were overwritten by the update sequence number the last time the containing structure was written to disk.</span></span>

<span data-ttu-id="84c06-126">Chaque fois que la structure protégée est sur le point d’être écrite sur le disque, le dernier mot de chaque Stride de numéro de séquence est enregistré à sa position respective dans le tableau des numéros de séquence, puis remplacé par le numéro de séquence de mise à jour suivant.</span><span class="sxs-lookup"><span data-stu-id="84c06-126">Each time the protected structure is about to be written to disk, the last word in each sequence number stride is saved to its respective position in the sequence number array, then it is overwritten with the next update sequence number.</span></span> <span data-ttu-id="84c06-127">Après l’écriture, ou chaque fois que la structure est lue, le mot enregistré du tableau des numéros de séquence est restauré à sa position réelle dans la structure.</span><span class="sxs-lookup"><span data-stu-id="84c06-127">After the write, or whenever the structure is read, the saved word from the sequence number array is restored to its actual position in the structure.</span></span> <span data-ttu-id="84c06-128">Avant de restaurer les mots enregistrés lors des lectures, tous les numéros de séquence à la fin de chaque Stride sont comparés au numéro de séquence réel au début du tableau.</span><span class="sxs-lookup"><span data-stu-id="84c06-128">Before restoring the saved words on reads, all the sequence numbers at the end of each stride are compared with the actual sequence number at the start of the array.</span></span> <span data-ttu-id="84c06-129">Si l’une de ces comparaisons n’est pas égale, un transfert multisecteur ayant échoué a été détecté.</span><span class="sxs-lookup"><span data-stu-id="84c06-129">If any of these comparisons are not equal, then a failed multisector transfer has been detected.</span></span>

<span data-ttu-id="84c06-130">La taille du tableau est déterminée par la taille de la structure conteneur.</span><span class="sxs-lookup"><span data-stu-id="84c06-130">The size of the array is determined by the size of the containing structure.</span></span> <span data-ttu-id="84c06-131">Le tableau de séquences de mise à jour doit être inclus à la fin de l’en-tête de la structure protégée en raison de sa taille variable.</span><span class="sxs-lookup"><span data-stu-id="84c06-131">The update sequence array should be included at the end of the header of the structure it is protecting because of its variable size.</span></span> <span data-ttu-id="84c06-132">L’utilisateur doit s’assurer que l’espace correct est réservé pour la structure conteneur : (taille de la structure/512 + 1) \* sizeof (UShort).</span><span class="sxs-lookup"><span data-stu-id="84c06-132">The user must ensure that the correct space is reserved for the containing structure: (size of structure / 512 + 1) \* sizeof(USHORT).</span></span>

## <a name="see-also"></a><span data-ttu-id="84c06-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84c06-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84c06-134">Table de fichiers maîtres</span><span class="sxs-lookup"><span data-stu-id="84c06-134">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
