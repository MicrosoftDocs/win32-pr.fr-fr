---
title: Clé ProgID indépendante de la version
description: Associe un ProgID à un CLSID. Cette clé est utilisée pour déterminer la dernière version d’une application d’objet.
ms.assetid: fb43c8d0-d923-487f-afdf-14fc29a71e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0a0bf379a06a6a05bb69a232ef91bb9fe81dc2f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464103"
---
# <a name="version-independent-progid-key"></a><span data-ttu-id="212b4-104">Clé ProgID indépendante de la version</span><span class="sxs-lookup"><span data-stu-id="212b4-104">version-independent ProgID Key</span></span>

<span data-ttu-id="212b4-105">Associe un ProgID à un CLSID.</span><span class="sxs-lookup"><span data-stu-id="212b4-105">Associates a ProgID with a CLSID.</span></span> <span data-ttu-id="212b4-106">Cette clé est utilisée pour déterminer la dernière version d’une application d’objet.</span><span class="sxs-lookup"><span data-stu-id="212b4-106">This key is used to determine the latest version of an object application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="212b4-107">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="212b4-107">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   <version-independent ProgID>
      CurVer = ProgID
```

## <a name="remarks"></a><span data-ttu-id="212b4-108">Notes</span><span class="sxs-lookup"><span data-stu-id="212b4-108">Remarks</span></span>

<span data-ttu-id="212b4-109">La clé de classes de logiciels de l' **\_ \_ ordinateur \\ \\ local HKEY** correspond à la clé **\_ \_ racine HKEY classes** , qui a été conservée pour la compatibilité avec les versions antérieures de com.</span><span class="sxs-lookup"><span data-stu-id="212b4-109">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

<span data-ttu-id="212b4-110">Le format pour <*ProgID indépendant* de la version> est <*programme*>. <*composant*>, séparé par des points, sans espace et sans numéro de version.</span><span class="sxs-lookup"><span data-stu-id="212b4-110">The format for <*version-independent ProgID*> is <*program*>.<*component*>, separated by periods, no spaces, and no version number.</span></span> <span data-ttu-id="212b4-111">Le ProgID indépendant de la version, comme le ProgID, peut être inscrit avec un nom explicite.</span><span class="sxs-lookup"><span data-stu-id="212b4-111">The version-independent ProgID, like the ProgID, can be registered with a human-readable name.</span></span>

<span data-ttu-id="212b4-112">*ProgID* est le ProgID de la dernière version installée de la classe.</span><span class="sxs-lookup"><span data-stu-id="212b4-112">*ProgID* is the ProgID of the latest installed version of the class.</span></span>

<span data-ttu-id="212b4-113">Les applications doivent inscrire un identificateur de programmation indépendant de la version sous la clé *ProgID indépendante* de la version.</span><span class="sxs-lookup"><span data-stu-id="212b4-113">Applications must register a version-independent programmatic identifier under the *version-independent ProgID* key.</span></span> <span data-ttu-id="212b4-114">Le ProgID indépendant de la version fait référence à la classe de l’application et ne passe pas de la version à la version, mais reste constante dans tous les versionsâ, par exemple, document Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="212b4-114">The version-independent ProgID refers to the application's class and does not change from version to version, instead remaining constant across all versionsâ€”for example, Microsoft Word Document.</span></span> <span data-ttu-id="212b4-115">Il est utilisé avec les langages de macro et fait référence à la version actuellement installée de la classe de l’application.</span><span class="sxs-lookup"><span data-stu-id="212b4-115">It is used with macro languages and refers to the currently installed version of the application's class.</span></span> <span data-ttu-id="212b4-116">Le ProgID indépendant de la version doit correspondre au nom de la version la plus récente de l’application objet.</span><span class="sxs-lookup"><span data-stu-id="212b4-116">The version-independent ProgID must correspond to the name of the latest version of the object application.</span></span>

<span data-ttu-id="212b4-117">Par exemple, le ProgID indépendant de la version est utilisé lorsqu’une application conteneur crée un graphique ou une table avec un bouton de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="212b4-117">For example, the version-independent ProgID is used when a container application creates a chart or table with a toolbar button.</span></span> <span data-ttu-id="212b4-118">Dans ce cas, l’application peut utiliser le ProgID indépendant de la version pour déterminer la version la plus récente de l’application objet nécessaire.</span><span class="sxs-lookup"><span data-stu-id="212b4-118">In this situation, the application can use the version-independent ProgID to determine the latest version of the needed object application.</span></span>

<span data-ttu-id="212b4-119">Le ProgID indépendant de la version est stocké et géré uniquement par le code d’application.</span><span class="sxs-lookup"><span data-stu-id="212b4-119">The version-independent ProgID is stored and maintained solely by application code.</span></span> <span data-ttu-id="212b4-120">Lorsqu’il reçoit le ProgID indépendant de la version, la fonction [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) retourne le CLSID de la version actuelle.</span><span class="sxs-lookup"><span data-stu-id="212b4-120">When given the version-independent ProgID, the [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) function returns the CLSID of the current version.</span></span>

<span data-ttu-id="212b4-121">Vous pouvez utiliser [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) et [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) pour effectuer une conversion entre ces deux représentations.</span><span class="sxs-lookup"><span data-stu-id="212b4-121">You can use [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) and [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) to convert between these two representations.</span></span>

<span data-ttu-id="212b4-122">Vous pouvez utiliser [**IOleObject :: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) ou [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype) pour remplacer l’identificateur par une chaîne affichable.</span><span class="sxs-lookup"><span data-stu-id="212b4-122">You can use [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) or [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype) to change the identifier to a displayable string.</span></span>

<span data-ttu-id="212b4-123">Si un gestionnaire personnalisé n’est pas utilisé, l’entrée doit être définie sur OLE32.DLL, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="212b4-123">If a custom handler is not used, the entry should be set to OLE32.DLL, as shown in the following example:</span></span>

```
HKEY_CLASSES_ROOT\CLSID\{00000402-0000-0000-C000-000000000046}
   InprocHandler = ole32.dll
```

## <a name="related-topics"></a><span data-ttu-id="212b4-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="212b4-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="212b4-125">**CLSIDFromProgID**</span><span class="sxs-lookup"><span data-stu-id="212b4-125">**CLSIDFromProgID**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid)
</dt> <dt>

[<span data-ttu-id="212b4-126">**ProgIDFromCLSID**</span><span class="sxs-lookup"><span data-stu-id="212b4-126">**ProgIDFromCLSID**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid)
</dt> <dt>

[<span data-ttu-id="212b4-127"><ProgID> Essentiel</span><span class="sxs-lookup"><span data-stu-id="212b4-127"><ProgID> Key</span></span>](-progid--key.md)
</dt> </dl>

 

 




