---
title: Clé ProgID
description: Un identificateur programmatique (ProgID) est une entrée de Registre qui peut être associée à un CLSID. À l’instar du CLSID, le ProgID identifie une classe mais avec moins de précision, car il n’est pas garanti qu’il soit globalement unique.
ms.assetid: f9ef2934-0815-4a6f-9283-8f748eee083b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a9ef64515d2dda4512af0086970cb2ab61b4830
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032226"
---
# <a name="progid-key"></a><span data-ttu-id="c35b3-104">Clé ProgID</span><span class="sxs-lookup"><span data-stu-id="c35b3-104">ProgID Key</span></span>

<span data-ttu-id="c35b3-105">Un identificateur programmatique (ProgID) est une entrée de Registre qui peut être associée à un CLSID.</span><span class="sxs-lookup"><span data-stu-id="c35b3-105">A programmatic identifier (ProgID) is a registry entry that can be associated with a CLSID.</span></span> <span data-ttu-id="c35b3-106">À l’instar du CLSID, le ProgID identifie une classe mais avec moins de précision, car il n’est pas garanti qu’il soit globalement unique.</span><span class="sxs-lookup"><span data-stu-id="c35b3-106">Like the CLSID, the ProgID identifies a class but with less precision because it is not guaranteed to be globally unique.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="c35b3-107">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="c35b3-107">Registry Entry</span></span>

<span data-ttu-id="c35b3-108">**HKEY \_ \_ \\ \\ Classes logicielles de l’ordinateur local** \\ *{* ProgID *}*</span><span class="sxs-lookup"><span data-stu-id="c35b3-108">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes**\\ *{* ProgID *}*</span></span>



| <span data-ttu-id="c35b3-109">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="c35b3-109">Registry key</span></span>                            | <span data-ttu-id="c35b3-110">Description</span><span class="sxs-lookup"><span data-stu-id="c35b3-110">Description</span></span>                                                        |
|-----------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="c35b3-111">**IDENTIFICATEUR**</span><span class="sxs-lookup"><span data-stu-id="c35b3-111">**CLSID**</span></span>](clsid.md)                  | <span data-ttu-id="c35b3-112">Associe un ProgID à un CLSID.</span><span class="sxs-lookup"><span data-stu-id="c35b3-112">Associates a ProgID with a CLSID.</span></span>                                  |
| [<span data-ttu-id="c35b3-113">**Insertable**</span><span class="sxs-lookup"><span data-stu-id="c35b3-113">**Insertable**</span></span>](insertable-progid.md) | <span data-ttu-id="c35b3-114">Indique que cette classe peut être insérée dans des conteneurs OLE 2.</span><span class="sxs-lookup"><span data-stu-id="c35b3-114">Indicates that this class is insertable in OLE 2 containers.</span></span>       |
| [<span data-ttu-id="c35b3-115">**Protocol**</span><span class="sxs-lookup"><span data-stu-id="c35b3-115">**Protocol**</span></span>](protocol.md)            | <span data-ttu-id="c35b3-116">Indique que cette classe OLE 2 peut être insérée dans les conteneurs OLE 1.</span><span class="sxs-lookup"><span data-stu-id="c35b3-116">Indicates that this OLE 2 class is insertable in OLE 1 containers.</span></span> |
| [<span data-ttu-id="c35b3-117">**Shell**</span><span class="sxs-lookup"><span data-stu-id="c35b3-117">**Shell**</span></span>](shell.md)                  | <span data-ttu-id="c35b3-118">Fournit les informations d’impression et d' **ouverture de fichier** du shell Windows 3,1.</span><span class="sxs-lookup"><span data-stu-id="c35b3-118">Provides Windows 3.1 shell printing and **File Open** information.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c35b3-119">Notes</span><span class="sxs-lookup"><span data-stu-id="c35b3-119">Remarks</span></span>

<span data-ttu-id="c35b3-120">Vous pouvez utiliser un ProgID dans des situations de programmation où il n’est pas possible d’utiliser un CLSID.</span><span class="sxs-lookup"><span data-stu-id="c35b3-120">You can use a ProgID in programming situations where it is not possible to use a CLSID.</span></span> <span data-ttu-id="c35b3-121">Les ProgID ne doivent pas apparaître dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c35b3-121">ProgIDs should not appear in the user interface.</span></span> <span data-ttu-id="c35b3-122">Il n’est pas garanti que les ProgID soient uniques, donc ils ne peuvent être utilisés que lorsque des collisions de noms sont gérables.</span><span class="sxs-lookup"><span data-stu-id="c35b3-122">ProgIDs are not guaranteed to be unique, so they can be used only where name collisions are manageable.</span></span>

<span data-ttu-id="c35b3-123">Le format d’un ProgID est <*programme*>. <*composant*>. <*version* , séparé par des points et sans espaces, comme dans> ument. 6.</span><span class="sxs-lookup"><span data-stu-id="c35b3-123">The format of a ProgID is <*Program*>.<*Component*>.<*Version*>, separated by periods and with no spaces, as in Word.Document.6.</span></span> <span data-ttu-id="c35b3-124">Le ProgID doit respecter les exigences suivantes :</span><span class="sxs-lookup"><span data-stu-id="c35b3-124">The ProgID must comply with the following requirements:</span></span>

-   <span data-ttu-id="c35b3-125">Ne pas comporter plus de 39 caractères.</span><span class="sxs-lookup"><span data-stu-id="c35b3-125">Have no more than 39 characters.</span></span>
-   <span data-ttu-id="c35b3-126">Ne pas contenir de signes de ponctuation (y compris les traits de soulignement), à l’exception d’un ou plusieurs points.</span><span class="sxs-lookup"><span data-stu-id="c35b3-126">Contain no punctuation (including underscores) except one or more periods.</span></span>
-   <span data-ttu-id="c35b3-127">Ne commence pas par un chiffre.</span><span class="sxs-lookup"><span data-stu-id="c35b3-127">Not start with a digit.</span></span>
-   <span data-ttu-id="c35b3-128">Être différent du nom de classe d’une application OLE 1, y compris la version OLE 1 de la même application, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="c35b3-128">Be different from the class name of any OLE 1 application, including the OLE 1 version of the same application, if there is one.</span></span>

<span data-ttu-id="c35b3-129">Étant donné que le ProgID ne doit pas apparaître dans l’interface utilisateur, vous pouvez obtenir un nom affichable en appelant [**IOleObject :: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype).</span><span class="sxs-lookup"><span data-stu-id="c35b3-129">Because the ProgID should not appear in the user interface, you can obtain a displayable name by calling [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype).</span></span> <span data-ttu-id="c35b3-130">Consultez également [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).</span><span class="sxs-lookup"><span data-stu-id="c35b3-130">Also, see [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).</span></span>

<span data-ttu-id="c35b3-131">La clé de classes de logiciels de l' **\_ \_ ordinateur \\ \\ local HKEY** correspond à la clé **\_ \_ racine HKEY classes** , qui a été conservée pour la compatibilité avec les versions antérieures de com.</span><span class="sxs-lookup"><span data-stu-id="c35b3-131">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c35b3-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c35b3-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c35b3-133">**IOleObject :: GetUserType**</span><span class="sxs-lookup"><span data-stu-id="c35b3-133">**IOleObject::GetUserType**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> <dt>

[<span data-ttu-id="c35b3-134">**OleRegGetUserType**</span><span class="sxs-lookup"><span data-stu-id="c35b3-134">**OleRegGetUserType**</span></span>](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype)
</dt> </dl>

 

 




