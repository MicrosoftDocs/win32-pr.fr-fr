---
description: Copie un certificat dans une chaîne encodée.
ms.assetid: bae7fb57-6b44-4aac-a635-b5b82de1f68d
title: 'ICertificate2 :: export, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Export
- ICertificate2.Export
- ICertificate.Export
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: aee48fe3d9ba56cba90c9645a3fb9752e3367a20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529986"
---
# <a name="icertificate2export-method"></a><span data-ttu-id="fa1fa-103">ICertificate2 :: export, méthode</span><span class="sxs-lookup"><span data-stu-id="fa1fa-103">ICertificate2::Export method</span></span>

<span data-ttu-id="fa1fa-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fa1fa-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="fa1fa-105">Utilisez plutôt la [**classe X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="fa1fa-105">Instead, use the [**X509Certificate2 Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="fa1fa-106">La méthode **Export** copie un certificat dans une chaîne encodée.</span><span class="sxs-lookup"><span data-stu-id="fa1fa-106">The **Export** method copies a certificate to an encoded string.</span></span> <span data-ttu-id="fa1fa-107">La chaîne encodée peut être écrite dans un fichier ou importée dans un nouvel objet de [**certificat**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="fa1fa-107">The encoded string can be written to a file or imported into a new [**Certificate**](certificate.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa1fa-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa1fa-108">Syntax</span></span>


```VB
Certificate.Export( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="fa1fa-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa1fa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa1fa-110">*EncodingType* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="fa1fa-110">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fa1fa-111">Valeur de l’énumération de [**\_ \_ type d’encodage**](capicom-encoding-type.md) CAPICOM qui spécifie le type d’encodage pour l’opération d’exportation.</span><span class="sxs-lookup"><span data-stu-id="fa1fa-111">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that specifies the encoding type for the export operation.</span></span> <span data-ttu-id="fa1fa-112">La valeur par défaut est **CAPICOM \_ encode \_ Base64**.</span><span class="sxs-lookup"><span data-stu-id="fa1fa-112">The default value is **CAPICOM\_ENCODE\_BASE64**.</span></span> <span data-ttu-id="fa1fa-113">Le tableau suivant répertorie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="fa1fa-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="fa1fa-114">Value</span><span class="sxs-lookup"><span data-stu-id="fa1fa-114">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="fa1fa-115">Signification</span><span class="sxs-lookup"><span data-stu-id="fa1fa-115">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="fa1fa-116"><dt>**\_coder \_ tout**</dt></span><span class="sxs-lookup"><span data-stu-id="fa1fa-116"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="fa1fa-117">Ce type d’encodage est utilisé uniquement lorsque les données d’entrée ont un type d’encodage inconnu.</span><span class="sxs-lookup"><span data-stu-id="fa1fa-117">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="fa1fa-118">Si cette valeur est utilisée pour spécifier le type d’encodage de la sortie, CAPICOM est utilisé à la \_ \_ place.</span><span class="sxs-lookup"><span data-stu-id="fa1fa-118">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="fa1fa-119">Introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="fa1fa-119">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="fa1fa-120"><dt>**\_Encode \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="fa1fa-120"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="fa1fa-121">Les données sont enregistrées sous la forme d’une chaîne encodée en base64.</span><span class="sxs-lookup"><span data-stu-id="fa1fa-121">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="fa1fa-122"><dt>**codage d’un \_ \_ fichier binaire CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="fa1fa-122"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="fa1fa-123">Les données sont enregistrées sous la forme d’une séquence binaire pure.</span><span class="sxs-lookup"><span data-stu-id="fa1fa-123">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa1fa-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fa1fa-124">Return value</span></span>

<span data-ttu-id="fa1fa-125">Chaîne qui contient le certificat exporté dans le formulaire d’encodage spécifié.</span><span class="sxs-lookup"><span data-stu-id="fa1fa-125">A string that contains the exported certificate in the specified encoding form.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa1fa-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa1fa-126">Requirements</span></span>



| <span data-ttu-id="fa1fa-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa1fa-127">Requirement</span></span> | <span data-ttu-id="fa1fa-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa1fa-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa1fa-129">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="fa1fa-129">End of client support</span></span><br/> | <span data-ttu-id="fa1fa-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa1fa-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fa1fa-131">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="fa1fa-131">End of server support</span></span><br/> | <span data-ttu-id="fa1fa-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa1fa-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fa1fa-133">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="fa1fa-133">Redistributable</span></span><br/>       | <span data-ttu-id="fa1fa-134">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="fa1fa-134">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fa1fa-135">DLL</span><span class="sxs-lookup"><span data-stu-id="fa1fa-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="fa1fa-136"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa1fa-136"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa1fa-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa1fa-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa1fa-138">Objets de chiffrement</span><span class="sxs-lookup"><span data-stu-id="fa1fa-138">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="fa1fa-139">**Certificat**</span><span class="sxs-lookup"><span data-stu-id="fa1fa-139">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
