---
description: Énumère tous les certificats sur le système qui correspondent aux critères indiqués et retourne une liste d’empreintes numériques.
ms.assetid: 69522afe-9870-4ae9-8c69-cf8787913615
title: Méthode FindValidCertificates de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.FindValidCertificates
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 69612d860284f6a47dfa38c2aafc3e73f209c796
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319878"
---
# <a name="findvalidcertificates-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="f524f-103">Méthode FindValidCertificates de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="f524f-103">FindValidCertificates method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="f524f-104">La méthode **FindValidCertificates** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) énumère tous les certificats du système qui correspondent aux critères indiqués et retourne une liste d’empreintes numériques.</span><span class="sxs-lookup"><span data-stu-id="f524f-104">The **FindValidCertificates** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class enumerates all certificates on the system that match the indicated criteria and returns a list of thumbprints.</span></span> <span data-ttu-id="f524f-105">La liste retournée contient uniquement des certificats avec un [*identificateur d’objet*](../secgloss/o-gly.md) (OID) valide.</span><span class="sxs-lookup"><span data-stu-id="f524f-105">The returned list only contains certificates with a valid [*object identifier*](../secgloss/o-gly.md) (OID).</span></span> <span data-ttu-id="f524f-106">L’OID peut être la valeur par défaut ou il peut être spécifié dans la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="f524f-106">The OID may be the default, or it may be specified in the Group Policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="f524f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f524f-107">Syntax</span></span>


```mof
uint32 FindValidCertificates(
  [out] string CertificateThumbprint[]
);
```



## <a name="parameters"></a><span data-ttu-id="f524f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f524f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f524f-109">*CertificateThumbprint* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f524f-109">*CertificateThumbprint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f524f-110">Type : **chaîne \[ \]**</span><span class="sxs-lookup"><span data-stu-id="f524f-110">Type: **string\[\]**</span></span>

<span data-ttu-id="f524f-111">Tableau de chaînes qui contient la liste des certificats valides.</span><span class="sxs-lookup"><span data-stu-id="f524f-111">An array of strings that contains the list of valid certificates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f524f-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f524f-112">Return value</span></span>

<span data-ttu-id="f524f-113">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f524f-113">Type: **uint32**</span></span>

<span data-ttu-id="f524f-114">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="f524f-114">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="f524f-115">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f524f-115">Return code/value</span></span>                                                                                                                                                                           | <span data-ttu-id="f524f-116">Description</span><span class="sxs-lookup"><span data-stu-id="f524f-116">Description</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="f524f-117"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="f524f-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                           | <span data-ttu-id="f524f-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="f524f-118">The method was successful.</span></span><br/>                |
| <dl> <span data-ttu-id="f524f-119"><dt>**FVE \_ E \_ \_ \_ OID BitLocker 2150695022 non valide**</dt> <dt>(0x8031006E)</dt></span><span class="sxs-lookup"><span data-stu-id="f524f-119"><dt>**FVE\_E\_INVALID\_BITLOCKER\_OID**</dt> <dt>2150695022 (0x8031006E)</dt></span></span> </dl> | <span data-ttu-id="f524f-120">L’OID BitLocker disponible n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f524f-120">The available BitLocker OID is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f524f-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f524f-121">Requirements</span></span>



| <span data-ttu-id="f524f-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f524f-122">Requirement</span></span> | <span data-ttu-id="f524f-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f524f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f524f-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f524f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f524f-125">Windows 7 entreprise, les applications de bureau Windows 7 édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f524f-125">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f524f-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f524f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f524f-127">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f524f-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f524f-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f524f-128">Namespace</span></span><br/>                | <span data-ttu-id="f524f-129">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="f524f-129">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="f524f-130">MOF</span><span class="sxs-lookup"><span data-stu-id="f524f-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f524f-131"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f524f-131"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f524f-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f524f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f524f-133">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="f524f-133">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
