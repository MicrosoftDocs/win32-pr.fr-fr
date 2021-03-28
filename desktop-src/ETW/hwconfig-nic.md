---
description: La \_ classe de carte réseau HWConfig est la classe de type d’événement pour les événements de configuration de carte d’interface réseau. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: e544a27b-17f8-402c-9c92-578cf2a38ca8
title: Classe HWConfig_NIC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_NIC
- HWConfig_NIC.NICName
api_type:
- NA
api_location: ''
ms.openlocfilehash: df3897c67ed65eeec5ace49dac1088ca35223a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035098"
---
# <a name="hwconfig_nic-class"></a><span data-ttu-id="d094e-104">\_Classe de carte réseau HWConfig</span><span class="sxs-lookup"><span data-stu-id="d094e-104">HWConfig\_NIC class</span></span>

<span data-ttu-id="d094e-105">La classe de **\_ carte réseau HWConfig** est la classe de type d’événement pour les événements de configuration de carte d’interface réseau.</span><span class="sxs-lookup"><span data-stu-id="d094e-105">The **HWConfig\_NIC** class is the event type class for network interface card configuration events.</span></span>

<span data-ttu-id="d094e-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="d094e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d094e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d094e-107">Syntax</span></span>

``` syntax
[EventType(13), EventTypeName("NIC")]
class HWConfig_NIC : HWConfig
{
  string NICName;
};
```

## <a name="members"></a><span data-ttu-id="d094e-108">Membres</span><span class="sxs-lookup"><span data-stu-id="d094e-108">Members</span></span>

<span data-ttu-id="d094e-109">La classe de **\_ carte réseau HWConfig** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d094e-109">The **HWConfig\_NIC** class has these types of members:</span></span>

-   [<span data-ttu-id="d094e-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d094e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d094e-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d094e-111">Properties</span></span>

<span data-ttu-id="d094e-112">La classe de **\_ carte réseau HWConfig** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d094e-112">The **HWConfig\_NIC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d094e-113">NICName</span><span class="sxs-lookup"><span data-stu-id="d094e-113">NICName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d094e-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d094e-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d094e-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d094e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d094e-116">Qualificateurs : WmiDataId (1), StringTermination ("NullTerminated"), format ("w")</span><span class="sxs-lookup"><span data-stu-id="d094e-116">Qualifiers: WmiDataId(1), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="d094e-117">Nom de la carte d’interface réseau.</span><span class="sxs-lookup"><span data-stu-id="d094e-117">Name of the network interface card.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d094e-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d094e-118">Requirements</span></span>



| <span data-ttu-id="d094e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d094e-119">Requirement</span></span> | <span data-ttu-id="d094e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d094e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="d094e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d094e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d094e-122">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d094e-122">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d094e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d094e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d094e-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d094e-124">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="d094e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d094e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d094e-126">**HWConfig**</span><span class="sxs-lookup"><span data-stu-id="d094e-126">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




