---
description: Définit ou récupère une valeur d’énumération qui spécifie le nom CAPICOM de l’utilisation améliorée de la valeur. Il s’agit de la propriété par défaut.
ms.assetid: afce5553-ef18-4a7f-b1c8-fbe00d3277e0
title: 'IEKU :: Name, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.Name
- IEKU.get_Name
- IEKU.put_Name
- EKU.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e0e28a8816d7e4c4f44e3cd1ec0dc479372d66d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525571"
---
# <a name="iekuname-property"></a><span data-ttu-id="d7ef6-104">IEKU :: Name, propriété</span><span class="sxs-lookup"><span data-stu-id="d7ef6-104">IEKU::Name property</span></span>

<span data-ttu-id="d7ef6-105">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d7ef6-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="d7ef6-106">Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="d7ef6-106">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="d7ef6-107">La propriété **Name** définit ou récupère une valeur d’énumération qui spécifie le nom CAPICOM de l’utilisation améliorée de la EKU.</span><span class="sxs-lookup"><span data-stu-id="d7ef6-107">The **Name** property sets or retrieves an enumeration value that specifies the CAPICOM name of the EKU.</span></span> <span data-ttu-id="d7ef6-108">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="d7ef6-108">This is the default property.</span></span>

<span data-ttu-id="d7ef6-109">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d7ef6-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7ef6-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7ef6-110">Syntax</span></span>


```VB
EKU.Name As CAPICOM_EKU
```



## <a name="property-value"></a><span data-ttu-id="d7ef6-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d7ef6-111">Property value</span></span>

<span data-ttu-id="d7ef6-112">Valeur de l’énumération [**\_ EKU de CAPICOM**](capicom-eku.md) qui spécifie le nom CAPICOM de l’utilisation améliorée de la variable.</span><span class="sxs-lookup"><span data-stu-id="d7ef6-112">A value of the [**CAPICOM\_EKU**](capicom-eku.md) enumeration that specifies the CAPICOM name of the EKU.</span></span> <span data-ttu-id="d7ef6-113">Le tableau suivant répertorie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="d7ef6-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="d7ef6-114">Value</span><span class="sxs-lookup"><span data-stu-id="d7ef6-114">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="d7ef6-115">Signification</span><span class="sxs-lookup"><span data-stu-id="d7ef6-115">Meaning</span></span>                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_EKU_OTHER"></span><span id="capicom_eku_other"></span><dl> <span data-ttu-id="d7ef6-116"><dt>**\_autre utilisation améliorée de la EKU \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d7ef6-116"><dt>**CAPICOM\_EKU\_OTHER**</dt></span></span> </dl>                                                      | <span data-ttu-id="d7ef6-117">Le certificat utilise le défini dans la stratégie locale.</span><span class="sxs-lookup"><span data-stu-id="d7ef6-117">Certificate has uses defined in local policy.</span></span> <span data-ttu-id="d7ef6-118">Utilisé si l’utilisation améliorée de la valeur requise n’est pas prédéfinie et que la valeur OID doit être définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="d7ef6-118">This is used if the EKU needed is not predefined and the OID value must be set by the application.</span></span><br/> |
| <span id="CAPICOM_EKU_SERVER_AUTH"></span><span id="capicom_eku_server_auth"></span><dl> <span data-ttu-id="d7ef6-119"><dt>**authentification du serveur de l' \_ utilisation améliorée de la EKU CAPICOM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d7ef6-119"><dt>**CAPICOM\_EKU\_SERVER\_AUTH**</dt></span></span> </dl>                                   | <span data-ttu-id="d7ef6-120">Le certificat peut être utilisé pour authentifier un serveur.</span><span class="sxs-lookup"><span data-stu-id="d7ef6-120">Certificate can be used to authenticate a server.</span></span><br/>                                                                                                |
| <span id="CAPICOM_EKU_CLIENT_AUTH"></span><span id="capicom_eku_client_auth"></span><dl> <span data-ttu-id="d7ef6-121"><dt>**authentification du client de l' \_ utilisation améliorée de la EKU CAPICOM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d7ef6-121"><dt>**CAPICOM\_EKU\_CLIENT\_AUTH**</dt></span></span> </dl>                                   | <span data-ttu-id="d7ef6-122">Le certificat peut être utilisé pour authentifier un client.</span><span class="sxs-lookup"><span data-stu-id="d7ef6-122">Certificate can be used to authenticate a client.</span></span><br/>                                                                                                |
| <span id="CAPICOM_EKU_CODE_SIGNING"></span><span id="capicom_eku_code_signing"></span><dl> <span data-ttu-id="d7ef6-123"><dt>**signature du code de l' \_ utilisation améliorée de la \_ \_ connexion**</dt></span><span class="sxs-lookup"><span data-stu-id="d7ef6-123"><dt>**CAPICOM\_EKU\_CODE\_SIGNING**</dt></span></span> </dl>                                | <span data-ttu-id="d7ef6-124">Le certificat peut être utilisé pour créer une signature numérique.</span><span class="sxs-lookup"><span data-stu-id="d7ef6-124">Certificate can be used to create a digital signature.</span></span><br/>                                                                                           |
| <span id="CAPICOM_EKU_EMAIL_PROTECTION"></span><span id="capicom_eku_email_protection"></span><dl> <span data-ttu-id="d7ef6-125"><dt>**\_protection par e-mail de l’utilisation améliorée de la \_ sécurité pour CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d7ef6-125"><dt>**CAPICOM\_EKU\_EMAIL\_PROTECTION**</dt></span></span> </dl>                    | <span data-ttu-id="d7ef6-126">Le certificat peut être utilisé pour la protection de la messagerie.</span><span class="sxs-lookup"><span data-stu-id="d7ef6-126">Certificate can be used for email protection.</span></span><br/>                                                                                                    |
| <span id="CAPICOM_EKU_SMARTCARD_LOGON"></span><span id="capicom_eku_smartcard_logon"></span><dl> <span data-ttu-id="d7ef6-127"><dt>**\_connexion par carte à \_ puce pour CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d7ef6-127"><dt>**CAPICOM\_EKU\_SMARTCARD\_LOGON**</dt></span></span> </dl>                       | <span data-ttu-id="d7ef6-128">Le certificat peut être utilisé pour l’ouverture de session par carte à puce.</span><span class="sxs-lookup"><span data-stu-id="d7ef6-128">Certificate can be used for smart card logon.</span></span> <span data-ttu-id="d7ef6-129">Introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="d7ef6-129">Introduced in CAPICOM 2.0.</span></span><br/>                                                                         |
| <span id="CAPICOM_EKU_ENCRYPTING_FILE_SYSTEM"></span><span id="capicom_eku_encrypting_file_system"></span><dl> <span data-ttu-id="d7ef6-130"><dt>**\_système de fichiers de \_ chiffrement \_ EKU \_ de CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="d7ef6-130"><dt>**CAPICOM\_EKU\_ENCRYPTING\_FILE\_SYSTEM**</dt></span></span> </dl> | <span data-ttu-id="d7ef6-131">Le certificat peut être utilisé pour EFS.</span><span class="sxs-lookup"><span data-stu-id="d7ef6-131">Certificate can be used for EFS.</span></span> <span data-ttu-id="d7ef6-132">Introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="d7ef6-132">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="d7ef6-133">Notes</span><span class="sxs-lookup"><span data-stu-id="d7ef6-133">Remarks</span></span>

<span data-ttu-id="d7ef6-134">Lorsque la valeur de cette propriété est réinitialisée, directement ou indirectement, l’intégralité de l' [*État*](../secgloss/s-gly.md) de l’objet est réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="d7ef6-134">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7ef6-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7ef6-135">Requirements</span></span>



| <span data-ttu-id="d7ef6-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7ef6-136">Requirement</span></span> | <span data-ttu-id="d7ef6-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7ef6-137">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7ef6-138">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="d7ef6-138">End of client support</span></span><br/> | <span data-ttu-id="d7ef6-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d7ef6-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d7ef6-140">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="d7ef6-140">End of server support</span></span><br/> | <span data-ttu-id="d7ef6-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d7ef6-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d7ef6-142">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="d7ef6-142">Redistributable</span></span><br/>       | <span data-ttu-id="d7ef6-143">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="d7ef6-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d7ef6-144">DLL</span><span class="sxs-lookup"><span data-stu-id="d7ef6-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d7ef6-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7ef6-145"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
