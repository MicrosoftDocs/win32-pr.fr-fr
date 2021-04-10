---
title: SID_IDENTIFIER_AUTHORITY
description: Définition du SID_IDENTIFIER_AUTHORITY IDL
ms.assetid: 88fe41f4-1c67-4290-ac21-fd43ff12d825
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: d9a80ed0717a279f39ac7a105a95807911232c82
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104102525"
---
# <a name="sid_identifier_authority-structure"></a><span data-ttu-id="d0282-103">Structure SID_IDENTIFIER_AUTHORITY</span><span class="sxs-lookup"><span data-stu-id="d0282-103">SID_IDENTIFIER_AUTHORITY structure</span></span>

<span data-ttu-id="d0282-104">Contient une autorité d’identificateur de SID.</span><span class="sxs-lookup"><span data-stu-id="d0282-104">Contains a SID identifier authority.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0282-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0282-105">Syntax</span></span>

```C++
typedef struct _SID_IDENTIFIER_AUTHORITY
{
    UCHAR Value[6];
} SID_IDENTIFIER_AUTHORITY, *PSID_IDENTIFIER_AUTHORITY;
```

## <a name="members"></a><span data-ttu-id="d0282-106">Membres</span><span class="sxs-lookup"><span data-stu-id="d0282-106">Members</span></span>

### <a name="value"></a><span data-ttu-id="d0282-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0282-107">Value</span></span>

<span data-ttu-id="d0282-108">Doit être défini sur les six octets de l’autorité d’identificateur SID.</span><span class="sxs-lookup"><span data-stu-id="d0282-108">Must be set to the six bytes of the SID identifier authority.</span></span>

## <a name="see-also"></a><span data-ttu-id="d0282-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0282-109">See also</span></span>

[<span data-ttu-id="d0282-110">**Définitions IDL de jonction de domaine hors connexion**</span><span class="sxs-lookup"><span data-stu-id="d0282-110">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)