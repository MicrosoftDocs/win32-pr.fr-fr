---
title: Méthode CreateSelfSignedCertificate de la classe Win32_TSGatewayServer
description: Crée un certificat auto-signé et retourne le hachage du certificat en tant que \ 0034 ; out \ 0034 ; paramètre.
ms.assetid: 2a5b8dee-50b8-44b7-9e29-25aff1c40f5d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode CreateSelfSignedCertificate
- Services Bureau à distance de la méthode CreateSelfSignedCertificate, classe Win32_TSGatewayServer
- Win32_TSGatewayServer de la classe Services Bureau à distance, méthode CreateSelfSignedCertificate
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.CreateSelfSignedCertificate
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4258566856a5fbc277053b65afe972751855d831
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464590"
---
# <a name="createselfsignedcertificate-method-of-the-win32_tsgatewayserver-class"></a><span data-ttu-id="c3a4e-106">Méthode CreateSelfSignedCertificate de la \_ classe Win32 TSGatewayServer</span><span class="sxs-lookup"><span data-stu-id="c3a4e-106">CreateSelfSignedCertificate method of the Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="c3a4e-107">Crée un certificat auto-signé et retourne le hachage du certificat en tant que paramètre « out ».</span><span class="sxs-lookup"><span data-stu-id="c3a4e-107">Creates a self-signed certificate and returns the certificate hash as an "out" parameter.</span></span> <span data-ttu-id="c3a4e-108">Ajoute également le texte « \_ \_ certificat auto- \_ signé de la passerelle TS \_ » à la propriété de contexte de certificat afin que le certificat soit reconnu en tant que certificat de passerelle des services Bureau à bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="c3a4e-108">Also, adds the text "TS\_GATEWAY\_SELF\_SIGNED\_CERTIFICATE" to the certificate context property so that the certificate is recognized as a Remote Desktop Gateway (RD Gateway) certificate.</span></span> <span data-ttu-id="c3a4e-109">Cette méthode utilise un conteneur de clé spécifique à la passerelle des services Bureau à distance pour créer le certificat.</span><span class="sxs-lookup"><span data-stu-id="c3a4e-109">This method uses an RD Gateway-specific key container to create the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3a4e-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3a4e-110">Syntax</span></span>


```mof
uint32 CreateSelfSignedCertificate(
  [in]  string SubjectName,
  [out] uint8  CertHash[]
);
```



## <a name="parameters"></a><span data-ttu-id="c3a4e-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3a4e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3a4e-112">*SubjectName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c3a4e-112">*SubjectName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3a4e-113">Nom du sujet du certificat auto-signé.</span><span class="sxs-lookup"><span data-stu-id="c3a4e-113">Subject name of the self-signed certificate.</span></span>

</dd> <dt>

<span data-ttu-id="c3a4e-114">*Certhash* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c3a4e-114">*CertHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3a4e-115">Hachage du certificat.</span><span class="sxs-lookup"><span data-stu-id="c3a4e-115">The certificate hash.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3a4e-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c3a4e-116">Remarks</span></span>

<span data-ttu-id="c3a4e-117">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="c3a4e-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="c3a4e-118">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="c3a4e-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c3a4e-119">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c3a4e-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c3a4e-120">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="c3a4e-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c3a4e-121">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c3a4e-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c3a4e-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3a4e-122">Requirements</span></span>



| <span data-ttu-id="c3a4e-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3a4e-123">Requirement</span></span> | <span data-ttu-id="c3a4e-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3a4e-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3a4e-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3a4e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c3a4e-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3a4e-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c3a4e-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3a4e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c3a4e-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3a4e-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c3a4e-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c3a4e-129">Namespace</span></span><br/>                | <span data-ttu-id="c3a4e-130">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="c3a4e-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c3a4e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c3a4e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3a4e-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c3a4e-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="c3a4e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c3a4e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3a4e-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3a4e-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c3a4e-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3a4e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3a4e-136">**\_TSGatewayServer Win32**</span><span class="sxs-lookup"><span data-stu-id="c3a4e-136">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> </dl>

 

