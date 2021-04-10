---
title: Méthode SetEncryptionLevel de la classe Win32_TSGeneralSetting
description: La méthode SetEncryptionLevel définit le niveau de chiffrement.
ms.assetid: 1822c4dc-bce6-489f-b21e-f96faffd2fa5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetEncryptionLevel
- Services Bureau à distance de la méthode SetEncryptionLevel, classe Win32_TSGeneralSetting
- Win32_TSGeneralSetting de la classe Services Bureau à distance, méthode SetEncryptionLevel
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetEncryptionLevel
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1fbe727c75851bb13252d196e1fe7d599f881c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104596"
---
# <a name="setencryptionlevel-method-of-the-win32_tsgeneralsetting-class"></a><span data-ttu-id="005ab-106">Méthode SetEncryptionLevel de la \_ classe Win32 TSGeneralSetting</span><span class="sxs-lookup"><span data-stu-id="005ab-106">SetEncryptionLevel method of the Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="005ab-107">La méthode **SetEncryptionLevel** définit le niveau de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="005ab-107">The **SetEncryptionLevel** method sets the encryption level.</span></span>

## <a name="syntax"></a><span data-ttu-id="005ab-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="005ab-108">Syntax</span></span>


```mof
uint32 SetEncryptionLevel(
  [in] uint32 MinEncryptionLevel
);
```



## <a name="parameters"></a><span data-ttu-id="005ab-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="005ab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="005ab-110">*MinEncryptionLevel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="005ab-110">*MinEncryptionLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="005ab-111">Niveau de chiffrement minimal à définir.</span><span class="sxs-lookup"><span data-stu-id="005ab-111">The minimum encryption level to set.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="005ab-112"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="005ab-112"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="005ab-113">Niveau de chiffrement faible.</span><span class="sxs-lookup"><span data-stu-id="005ab-113">Low level of encryption.</span></span> <span data-ttu-id="005ab-114">Seules les données envoyées du client au serveur sont chiffrées à l’aide du chiffrement 56 bits.</span><span class="sxs-lookup"><span data-stu-id="005ab-114">Only data sent from the client to the server is encrypted using 56-bit encryption.</span></span> <span data-ttu-id="005ab-115">Notez que les données envoyées du serveur au client ne sont pas chiffrées.</span><span class="sxs-lookup"><span data-stu-id="005ab-115">Note that data sent from the server to the client is not encrypted.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="005ab-116"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="005ab-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="005ab-117">Niveau de chiffrement compatible avec le client.</span><span class="sxs-lookup"><span data-stu-id="005ab-117">Client-compatible level of encryption.</span></span> <span data-ttu-id="005ab-118">Toutes les données envoyées du client au serveur et du serveur au client sont chiffrées au niveau de clé maximal pris en charge par le client.</span><span class="sxs-lookup"><span data-stu-id="005ab-118">All data sent from client to server and from server to client is encrypted at the maximum key strength supported by the client.</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="005ab-119"><span id="3"></span>**1,3**</span><span class="sxs-lookup"><span data-stu-id="005ab-119"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="005ab-120">Niveau élevé de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="005ab-120">High level of encryption.</span></span> <span data-ttu-id="005ab-121">Toutes les données envoyées du client au serveur et du serveur au client sont chiffrées à l’aide d’un chiffrement 128 bits puissant.</span><span class="sxs-lookup"><span data-stu-id="005ab-121">All data sent from client to server and from server to client is encrypted using strong 128-bit encryption.</span></span> <span data-ttu-id="005ab-122">Les clients qui ne prennent pas en charge ce niveau de chiffrement ne peuvent pas se connecter.</span><span class="sxs-lookup"><span data-stu-id="005ab-122">Clients that do not support this level of encryption cannot connect.</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="005ab-123"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="005ab-123"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="005ab-124">Chiffrement conforme à la norme FIPS.</span><span class="sxs-lookup"><span data-stu-id="005ab-124">FIPS-compliant encryption.</span></span> <span data-ttu-id="005ab-125">Toutes les données envoyées du client au serveur et du serveur au client sont chiffrées et déchiffrées avec les algorithmes de chiffrement normes FIPS (Federal Information Processing Standard) (FIPS) à l’aide des modules de chiffrement Microsoft.</span><span class="sxs-lookup"><span data-stu-id="005ab-125">All data sent from client to server and from server to client is encrypted and decrypted with the Federal Information Processing Standard (FIPS) encryption algorithms using the Microsoft cryptographic modules.</span></span> <span data-ttu-id="005ab-126">FIPS est une norme intitulée « exigences de sécurité pour les modules cryptographiques ».</span><span class="sxs-lookup"><span data-stu-id="005ab-126">FIPS is a standard entitled "Security Requirements for Cryptographic Modules".</span></span> <span data-ttu-id="005ab-127">FIPS 140-1 (1994) et FIPS 140-2 (2001) décrivent les exigences gouvernementales pour les modules de chiffrement matériels et logiciels utilisés au sein du gouvernement des États-Unis.</span><span class="sxs-lookup"><span data-stu-id="005ab-127">FIPS 140-1 (1994) and FIPS 140-2 (2001) describe government requirements for hardware and software cryptographic modules used within the U.S. government.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="005ab-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="005ab-128">Return value</span></span>

<span data-ttu-id="005ab-129">Retourne une réussite en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="005ab-129">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="005ab-130">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="005ab-130">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="005ab-131">Notes</span><span class="sxs-lookup"><span data-stu-id="005ab-131">Remarks</span></span>

<span data-ttu-id="005ab-132">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="005ab-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="005ab-133">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="005ab-133">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="005ab-134">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="005ab-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="005ab-135">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="005ab-135">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="005ab-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="005ab-136">Requirements</span></span>



| <span data-ttu-id="005ab-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="005ab-137">Requirement</span></span> | <span data-ttu-id="005ab-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="005ab-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="005ab-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="005ab-139">Minimum supported client</span></span><br/> | <span data-ttu-id="005ab-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="005ab-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="005ab-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="005ab-141">Minimum supported server</span></span><br/> | <span data-ttu-id="005ab-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="005ab-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="005ab-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="005ab-143">Namespace</span></span><br/>                | <span data-ttu-id="005ab-144">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="005ab-144">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="005ab-145">MOF</span><span class="sxs-lookup"><span data-stu-id="005ab-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="005ab-146"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="005ab-146"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="005ab-147">DLL</span><span class="sxs-lookup"><span data-stu-id="005ab-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="005ab-148"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="005ab-148"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="005ab-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="005ab-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="005ab-150">**\_TSGeneralSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="005ab-150">**Win32\_TSGeneralSetting**</span></span>](win32-tsgeneralsetting.md)
</dt> </dl>

 

