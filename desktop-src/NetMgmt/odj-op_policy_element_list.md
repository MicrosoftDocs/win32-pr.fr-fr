---
title: OP_POLICY_ELEMENT_LIST
description: Définition du OP_POLICY_ELEMENT_LIST IDL
ms.assetid: 1eebbdd2-655b-4bd3-938c-6bc687ffe7bb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 3c46e7208e6c142b9f58a7704be9bd3461c845b2
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "103734700"
---
# <a name="op_policy_element_list-structure"></a><span data-ttu-id="8c2e4-103">Structure OP_POLICY_ELEMENT_LIST</span><span class="sxs-lookup"><span data-stu-id="8c2e4-103">OP_POLICY_ELEMENT_LIST structure</span></span>

<span data-ttu-id="8c2e4-104">Définit une clé de Registre racine et un tableau d’éléments de clé de Registre à configurer sous cette clé.</span><span class="sxs-lookup"><span data-stu-id="8c2e4-104">Defines  a root registry key and an array of registry key elements to be configured under that key.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c2e4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c2e4-105">Syntax</span></span>

```C++
typedef struct _OP_POLICY_ELEMENT_LIST
{
    [string] wchar_t                            *pSource;
    ULONG                                       ulRootKeyId;
    ULONG                                       cElements;
    [size_is(cElements)]    POP_POLICY_ELEMENT  pElements;
} OP_POLICY_ELEMENT_LIST, *POP_POLICY_ELEMENT_LIST;
```

## <a name="members"></a><span data-ttu-id="8c2e4-106">Membres</span><span class="sxs-lookup"><span data-stu-id="8c2e4-106">Members</span></span>

### <a name="psource"></a><span data-ttu-id="8c2e4-107">pSource</span><span class="sxs-lookup"><span data-stu-id="8c2e4-107">pSource</span></span>

<span data-ttu-id="8c2e4-108">Contient le chemin d’accès du fichier stratégie de groupe à partir duquel les éléments contenus ont été issus.</span><span class="sxs-lookup"><span data-stu-id="8c2e4-108">Contains the path of the Group Policy file that the contained elements were sourced from.</span></span>

### <a name="ulrootkeyid"></a><span data-ttu-id="8c2e4-109">ulRootKeyId</span><span class="sxs-lookup"><span data-stu-id="8c2e4-109">ulRootKeyId</span></span>

<span data-ttu-id="8c2e4-110">Contient l’identificateur de la clé de Registre racine ; doit être défini sur HKEY_LOCAL_MACHINE.</span><span class="sxs-lookup"><span data-stu-id="8c2e4-110">Contains the identifier of the root registry key; currently must be set to HKEY_LOCAL_MACHINE.</span></span>

### <a name="celements"></a><span data-ttu-id="8c2e4-111">cElements</span><span class="sxs-lookup"><span data-stu-id="8c2e4-111">cElements</span></span>

<span data-ttu-id="8c2e4-112">Contient le nombre d’éléments dans les papelements.</span><span class="sxs-lookup"><span data-stu-id="8c2e4-112">Contains the number of elements in pElements.</span></span>

### <a name="pelements"></a><span data-ttu-id="8c2e4-113">papelements</span><span class="sxs-lookup"><span data-stu-id="8c2e4-113">pElements</span></span>

<span data-ttu-id="8c2e4-114">Contient un tableau d’éléments OP_POLICY_ELEMENT.</span><span class="sxs-lookup"><span data-stu-id="8c2e4-114">Contains an array of OP_POLICY_ELEMENT elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="8c2e4-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c2e4-115">See also</span></span>

[<span data-ttu-id="8c2e4-116">**Définitions IDL de jonction de domaine hors connexion**</span><span class="sxs-lookup"><span data-stu-id="8c2e4-116">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="8c2e4-117">**OP ( \_ élément de stratégie) \_**</span><span class="sxs-lookup"><span data-stu-id="8c2e4-117">**OP\_POLICY\_ELEMENT**</span></span>](odj-op_policy_element.md)
