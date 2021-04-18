---
description: Modifie les informations d’identification d’autorisation du propriétaire de l’appareil TPM. Les anciens et nouveaux mots de passe d’autorisation du propriétaire sont requis.
ms.assetid: 5b7f1aec-5181-4330-982c-d80a1d5ae9e8
title: Méthode ChangeOwnerAuth de la classe CIM_TPM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM.ChangeOwnerAuth
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2d5a2895e6a0049b2284b55aea1dc9a1849341c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519848"
---
# <a name="changeownerauth-method-of-the-cim_tpm-class"></a><span data-ttu-id="54343-104">Méthode ChangeOwnerAuth de la \_ classe TPM CIM</span><span class="sxs-lookup"><span data-stu-id="54343-104">ChangeOwnerAuth method of the CIM\_TPM class</span></span>

<span data-ttu-id="54343-105">Modifie les informations d’identification d’autorisation du propriétaire de l’appareil TPM.</span><span class="sxs-lookup"><span data-stu-id="54343-105">Changes the owner authorization credential of the TPM device.</span></span> <span data-ttu-id="54343-106">Les anciens et nouveaux mots de passe d’autorisation du propriétaire sont requis.</span><span class="sxs-lookup"><span data-stu-id="54343-106">The old and new owner authorization passwords are required.</span></span>

## <a name="syntax"></a><span data-ttu-id="54343-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54343-107">Syntax</span></span>


```mof
uint32 ChangeOwnerAuth(
  [in] string OldOwnerAuth,
  [in] string NewOwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="54343-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54343-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54343-109">*OldOwnerAuth* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="54343-109">*OldOwnerAuth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54343-110">Représente les anciennes informations d’identification d’autorisation du propriétaire requises pour prendre possession du périphérique TPM. La sous-classe **CIM \_ SharedCredential** peut être requise avec la valeur non null du **\_ SharedCredential CIM**.**Propriété secrète** pour le paramètre.</span><span class="sxs-lookup"><span data-stu-id="54343-110">Represents the old owner authorization credential required to take ownership of the TPM device.The **CIM\_SharedCredential** subclass may be required with non-null value of the **CIM\_SharedCredential**.**Secret** property for the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="54343-111">*NewOwnerAuth* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="54343-111">*NewOwnerAuth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54343-112">Représente les informations d’identification d’autorisation du nouveau propriétaire requises pour prendre possession du périphérique TPM. La sous-classe **CIM \_ SharedCredential** peut être requise avec la valeur non null du **\_ SharedCredential CIM**.**Propriété secrète** pour le paramètre.</span><span class="sxs-lookup"><span data-stu-id="54343-112">Represents the new owner authorization credential required to take ownership of the TPM device.The **CIM\_SharedCredential** subclass may be required with non-null value of the **CIM\_SharedCredential**.**Secret** property for the parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54343-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="54343-113">Return value</span></span>

<span data-ttu-id="54343-114">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="54343-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="54343-115">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="54343-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="54343-116">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="54343-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="54343-117">**Erreur inconnue/non spécifiée** (2)</span><span class="sxs-lookup"><span data-stu-id="54343-117">**Unknown/Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="54343-118">**DMTF réservé** (3.. 4095)</span><span class="sxs-lookup"><span data-stu-id="54343-118">**DMTF Reserved** (3..4095)</span></span>
</dt> <dt>

<span data-ttu-id="54343-119">**Méthode réservée** (4096.. 32767)</span><span class="sxs-lookup"><span data-stu-id="54343-119">**Method Reserved** (4096..32767)</span></span>
</dt> <dt>

<span data-ttu-id="54343-120">**Fournisseur spécifié** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="54343-120">**Vendor Specified** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="54343-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54343-121">Requirements</span></span>



| <span data-ttu-id="54343-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54343-122">Requirement</span></span> | <span data-ttu-id="54343-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="54343-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54343-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54343-124">Minimum supported client</span></span><br/> | <span data-ttu-id="54343-125">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54343-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="54343-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54343-126">Minimum supported server</span></span><br/> | <span data-ttu-id="54343-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="54343-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="54343-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="54343-128">Namespace</span></span><br/>                | <span data-ttu-id="54343-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="54343-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="54343-130">MOF</span><span class="sxs-lookup"><span data-stu-id="54343-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54343-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="54343-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="54343-132">DLL</span><span class="sxs-lookup"><span data-stu-id="54343-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54343-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="54343-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="54343-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54343-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54343-135">**\_TPM CIM**</span><span class="sxs-lookup"><span data-stu-id="54343-135">**CIM\_TPM**</span></span>](cim-tpm.md)
</dt> </dl>

 

 




