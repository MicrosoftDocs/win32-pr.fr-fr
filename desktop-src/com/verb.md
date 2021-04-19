---
title: Verbe
description: Spécifie les verbes à inscrire pour une application.
ms.assetid: bfcad36d-a52a-4117-bf0b-6135b197a7ee
keywords:
- Clé de Registre Verb COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ef025ee0807ca3e75577f26f81951db22dfb0ac
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106530798"
---
# <a name="verb"></a><span data-ttu-id="cba4c-104">Verbe</span><span class="sxs-lookup"><span data-stu-id="cba4c-104">Verb</span></span>

<span data-ttu-id="cba4c-105">Spécifie les verbes à inscrire pour une application.</span><span class="sxs-lookup"><span data-stu-id="cba4c-105">Specifies the verbs to be registered for an application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="cba4c-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="cba4c-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Verb
         1 = verb1
         2 = verb2
         3 = ...
```

## <a name="remarks"></a><span data-ttu-id="cba4c-107">Notes</span><span class="sxs-lookup"><span data-stu-id="cba4c-107">Remarks</span></span>

<span data-ttu-id="cba4c-108">Chaque verbe est une **valeur \_ reg SZ** au format «*nom*, *\_ indicateur de menu*, *\_ indicateur de verbe*».</span><span class="sxs-lookup"><span data-stu-id="cba4c-108">Each verb is a **REG\_SZ** value of the form "*name*, *menu\_flag*, *verb\_flag*".</span></span> <span data-ttu-id="cba4c-109">Les verbes doivent être numérotés de manière consécutive.</span><span class="sxs-lookup"><span data-stu-id="cba4c-109">Verbs must be numbered consecutively.</span></span>

<span data-ttu-id="cba4c-110">Le *nom* décrit comment le verbe est ajouté par un appel de fonction [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) .</span><span class="sxs-lookup"><span data-stu-id="cba4c-110">The *name* describes how the verb is appended by an [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) function call.</span></span> <span data-ttu-id="cba4c-111">Par exemple, « &Play ».</span><span class="sxs-lookup"><span data-stu-id="cba4c-111">For example, "&Play".</span></span>

<span data-ttu-id="cba4c-112">La valeur de l' *\_ indicateur de menu* indique comment le verbe doit apparaître dans le menu.</span><span class="sxs-lookup"><span data-stu-id="cba4c-112">The *menu\_flag* value indicates how the verb should appear in the menu.</span></span> <span data-ttu-id="cba4c-113">Tous les indicateurs pris en charge par [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) sont pris en charge, à l’exception des \_ bitmaps MF, MF \_ OwnerDraw et MF \_ .</span><span class="sxs-lookup"><span data-stu-id="cba4c-113">All flags supported by [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) are supported, except for MF\_BITMAP, MF\_OWNERDRAW, and MF\_POPUP.</span></span>

<span data-ttu-id="cba4c-114">La valeur de l' *\_ indicateur de verbe* décrit les attributs des verbes.</span><span class="sxs-lookup"><span data-stu-id="cba4c-114">The *verb\_flag* value describes attributes of the verbs.</span></span> <span data-ttu-id="cba4c-115">Utilisez l’une des valeurs de [**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib), ou 0.</span><span class="sxs-lookup"><span data-stu-id="cba4c-115">Use one of the values from [**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib), or 0.</span></span>

<span data-ttu-id="cba4c-116">Pour plus d’informations, consultez [**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb), [**IOleObject ::D overb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)et [**IOleObject :: EnumVerbs**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-enumverbs).</span><span class="sxs-lookup"><span data-stu-id="cba4c-116">For more information, see [**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb), [**IOleObject::DoVerb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb), and [**IOleObject::EnumVerbs**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-enumverbs).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cba4c-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cba4c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cba4c-118">**AppendMenu**</span><span class="sxs-lookup"><span data-stu-id="cba4c-118">**AppendMenu**</span></span>](/windows/win32/api/winuser/nf-winuser-appendmenua)
</dt> <dt>

[<span data-ttu-id="cba4c-119">**OLEVERB**</span><span class="sxs-lookup"><span data-stu-id="cba4c-119">**OLEVERB**</span></span>](/windows/win32/api/oleidl/ns-oleidl-oleverb)
</dt> <dt>

[<span data-ttu-id="cba4c-120">**OLEVERBATTRIB**</span><span class="sxs-lookup"><span data-stu-id="cba4c-120">**OLEVERBATTRIB**</span></span>](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)
</dt> </dl>

 

 