---
description: Contient des informations sur les boutons personnalisés à ajouter à la barre d’outils du gestionnaire de fichiers. Les boutons sont fournis par une DLL d’extension du gestionnaire de fichiers.
title: Structure FMS_TOOLBARLOAD (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_TOOLBARLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 7185f9e5-10c6-43cc-b85b-cd077378338f
ms.openlocfilehash: 8e123c759a827adddf5fd00eaf33193ebca0dbf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973219"
---
# <a name="fms_toolbarload-structure"></a><span data-ttu-id="e143e-104">\_TOOLBARLOAD-structure FMS</span><span class="sxs-lookup"><span data-stu-id="e143e-104">FMS\_TOOLBARLOAD structure</span></span>

<span data-ttu-id="e143e-105">Contient des informations sur les boutons personnalisés à ajouter à la barre d’outils du gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e143e-105">Contains information about custom buttons to be added to the File Manager toolbar.</span></span> <span data-ttu-id="e143e-106">Les boutons sont fournis par une DLL d’extension du gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e143e-106">The buttons are provided by a File Manager extension DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="e143e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e143e-107">Syntax</span></span>


```C++
typedef struct _FMS_TOOLBARLOAD {
  DWORD        dwSize;
  LPEXT_BUTTON lpButtons;
  WORD         cButtons;
  WORD         cBitmaps;
  WORD         idBitmap;
  HBITMAP      hBitmap;
} FMS_TOOLBARLOAD;
```



## <a name="members"></a><span data-ttu-id="e143e-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e143e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e143e-109">**dwSize nul**</span><span class="sxs-lookup"><span data-stu-id="e143e-109">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="e143e-110">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e143e-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e143e-111">Taille, en octets, de la structure.</span><span class="sxs-lookup"><span data-stu-id="e143e-111">The size, in bytes, of the structure.</span></span> <span data-ttu-id="e143e-112">Le gestionnaire de fichiers définit la taille avant d’appeler l’extension et vérifie la taille après le retour de la procédure d’extension.</span><span class="sxs-lookup"><span data-stu-id="e143e-112">File Manager sets the size before calling the extension and checks the size after the extension procedure returns.</span></span>

</dd> <dt>

<span data-ttu-id="e143e-113">**lpButtons**</span><span class="sxs-lookup"><span data-stu-id="e143e-113">**lpButtons**</span></span>
</dt> <dd>

<span data-ttu-id="e143e-114">Type : **LPEXT \_ Button**</span><span class="sxs-lookup"><span data-stu-id="e143e-114">Type: **LPEXT\_BUTTON**</span></span>

</dd> <dd>

<span data-ttu-id="e143e-115">Adresse d’un tableau de structures [**de \_ bouton ext**](ext-button.md) .</span><span class="sxs-lookup"><span data-stu-id="e143e-115">The address of an array of [**EXT\_BUTTON**](ext-button.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="e143e-116">**cButtons**</span><span class="sxs-lookup"><span data-stu-id="e143e-116">**cButtons**</span></span>
</dt> <dd>

<span data-ttu-id="e143e-117">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="e143e-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e143e-118">Nombre de structures [**de \_ bouton ext**](ext-button.md) dans le tableau vers lequel pointe le membre **lpButtons** .</span><span class="sxs-lookup"><span data-stu-id="e143e-118">The number of [**EXT\_BUTTON**](ext-button.md) structures in the array pointed to by the **lpButtons** member.</span></span> <span data-ttu-id="e143e-119">Ce nombre est égal au nombre de boutons et de séparateurs à ajouter à la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="e143e-119">This number equals the number of buttons and separators to add to the toolbar.</span></span>

</dd> <dt>

<span data-ttu-id="e143e-120">**cBitmaps**</span><span class="sxs-lookup"><span data-stu-id="e143e-120">**cBitmaps**</span></span>
</dt> <dd>

<span data-ttu-id="e143e-121">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="e143e-121">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e143e-122">Nombre de boutons représentés par la bitmap donnée.</span><span class="sxs-lookup"><span data-stu-id="e143e-122">The number of buttons represented by the given bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="e143e-123">**idBitmap**</span><span class="sxs-lookup"><span data-stu-id="e143e-123">**idBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="e143e-124">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="e143e-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e143e-125">Identificateur d’une ressource bitmap dans le fichier exécutable de la DLL d’extension.</span><span class="sxs-lookup"><span data-stu-id="e143e-125">The identifier of a bitmap resource in the executable file for the extension DLL.</span></span> <span data-ttu-id="e143e-126">La ressource bitmap contient des images pour le nombre de boutons spécifiés par **cBitmaps**.</span><span class="sxs-lookup"><span data-stu-id="e143e-126">The bitmap resource contains images for the number of buttons specified by **cBitmaps**.</span></span> <span data-ttu-id="e143e-127">Le gestionnaire de fichiers charge la ressource bitmap, puis l’utilise pour afficher les boutons.</span><span class="sxs-lookup"><span data-stu-id="e143e-127">File Manager loads the bitmap resource and then uses it to display the buttons.</span></span>

</dd> <dt>

<span data-ttu-id="e143e-128">**hBitmap**</span><span class="sxs-lookup"><span data-stu-id="e143e-128">**hBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="e143e-129">Type : **HBITMAP**</span><span class="sxs-lookup"><span data-stu-id="e143e-129">Type: **HBITMAP**</span></span>

</dd> <dd>

<span data-ttu-id="e143e-130">Handle d’une image bitmap que le gestionnaire de fichiers utilisera pour obtenir et afficher des images de bouton si **idBitmap** est égal à 0.</span><span class="sxs-lookup"><span data-stu-id="e143e-130">A handle to a bitmap that File Manager will use to obtain and display button images if **idBitmap** is 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e143e-131">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e143e-131">Requirements</span></span>



| <span data-ttu-id="e143e-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e143e-132">Requirement</span></span> | <span data-ttu-id="e143e-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="e143e-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e143e-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e143e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e143e-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e143e-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e143e-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e143e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e143e-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e143e-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e143e-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="e143e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="e143e-139"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="e143e-139"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e143e-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e143e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e143e-141">**FMEVENT \_ TOOLBARLOAD**</span><span class="sxs-lookup"><span data-stu-id="e143e-141">**FMEVENT\_TOOLBARLOAD**</span></span>](fmevent-toolbarload.md)
</dt> </dl>

 

 




