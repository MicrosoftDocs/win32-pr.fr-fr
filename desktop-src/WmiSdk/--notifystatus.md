---
description: Sert de classe parente pour les classes d’erreur définies par le fournisseur.
ms.assetid: fc2747f5-cfbc-4d61-894d-4585a03dda3f
ms.tgt_platform: multiple
title: Classe __NotifyStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NotifyStatus
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: f19ef1f6088b5a058f4483f197877358177c81f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759441"
---
# <a name="__notifystatus-class"></a><span data-ttu-id="6f1ee-103">\_\_NotifyStatus, classe</span><span class="sxs-lookup"><span data-stu-id="6f1ee-103">\_\_NotifyStatus class</span></span>

<span data-ttu-id="6f1ee-104">La classe système abstraite **\_ \_ NotifyStatus** sert de classe parente pour les classes d’erreur définies par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="6f1ee-104">The **\_\_NotifyStatus** abstract system class serves as the parent class for provider-defined error classes.</span></span>

<span data-ttu-id="6f1ee-105">La syntaxe suivante est simplifiée du code format MOF (MF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6f1ee-105">The following syntax is simplified from Managed Object Format (MF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f1ee-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f1ee-106">Syntax</span></span>

``` syntax
[abstract]
class __NotifyStatus
{
  uint32 StatusCode;
};
```

## <a name="members"></a><span data-ttu-id="6f1ee-107">Membres</span><span class="sxs-lookup"><span data-stu-id="6f1ee-107">Members</span></span>

<span data-ttu-id="6f1ee-108">La classe **\_ \_ NotifyStatus** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6f1ee-108">The **\_\_NotifyStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="6f1ee-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6f1ee-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6f1ee-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6f1ee-110">Properties</span></span>

<span data-ttu-id="6f1ee-111">La classe **\_ \_ NotifyStatus** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="6f1ee-111">The **\_\_NotifyStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6f1ee-112">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="6f1ee-112">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1ee-113">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6f1ee-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f1ee-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1ee-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f1ee-115">Contient une erreur ou un code d’information pour une opération.</span><span class="sxs-lookup"><span data-stu-id="6f1ee-115">Contains an error or information code for an operation.</span></span> <span data-ttu-id="6f1ee-116">Il peut s’agir de n’importe quel code défini par l’utilisateur, mais la valeur 0 (zéro) est généralement réservée pour indiquer la réussite de l’opération.</span><span class="sxs-lookup"><span data-stu-id="6f1ee-116">This can be any user-defined code, but the value 0 (zero) is usually reserved to indicate success.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6f1ee-117">Notes</span><span class="sxs-lookup"><span data-stu-id="6f1ee-117">Remarks</span></span>

<span data-ttu-id="6f1ee-118">Bien que la classe **\_ \_ NotifyStatus** puisse être la classe parente pour les classes d’erreur définies par le fournisseur, il est recommandé que les fournisseurs dérivent les classes d’erreur de [**\_ \_ ExtendedStatus**](--extendedstatus.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="6f1ee-118">Although the **\_\_NotifyStatus** class can be the parent class for provider-defined error classes, it is recommended that providers derive error classes from [**\_\_ExtendedStatus**](--extendedstatus.md) instead.</span></span> <span data-ttu-id="6f1ee-119">L’utilisation de **\_ \_ ExtendedStatus** permet une plus grande normalisation des classes d’erreur.</span><span class="sxs-lookup"><span data-stu-id="6f1ee-119">Using **\_\_ExtendedStatus** allows for greater standardization of error classes.</span></span>

<span data-ttu-id="6f1ee-120">Les fournisseurs ne doivent jamais créer des instances de **\_ \_ NotifyStatus** directement, car ces instances ne transmettent pas plus d’informations qu’un simple code de retour.</span><span class="sxs-lookup"><span data-stu-id="6f1ee-120">Providers should never create instances of **\_\_NotifyStatus** directly, because these instances convey no more information than a simple return code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f1ee-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f1ee-121">Requirements</span></span>



| <span data-ttu-id="6f1ee-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f1ee-122">Requirement</span></span> | <span data-ttu-id="6f1ee-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f1ee-123">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="6f1ee-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f1ee-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6f1ee-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f1ee-125">Windows Vista</span></span><br/>       |
| <span data-ttu-id="6f1ee-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f1ee-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6f1ee-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f1ee-127">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="6f1ee-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6f1ee-128">Namespace</span></span><br/>                | <span data-ttu-id="6f1ee-129">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="6f1ee-129">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="6f1ee-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f1ee-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f1ee-131">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="6f1ee-131">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




