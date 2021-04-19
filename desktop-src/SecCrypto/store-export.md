---
description: Copie le contenu d’un magasin de certificats ouvert dans une chaîne encodée.
ms.assetid: 00697579-f929-42ed-8e8e-5c970fe4465b
title: Store. Export, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Export
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dbf4a2912cb62935447daa1589b6829c5a96488e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525591"
---
# <a name="storeexport-method"></a><span data-ttu-id="50b89-103">Store. Export, méthode</span><span class="sxs-lookup"><span data-stu-id="50b89-103">Store.Export method</span></span>

<span data-ttu-id="50b89-104">\[La méthode d' **exportation** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="50b89-104">\[The **Export** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="50b89-105">Utilisez plutôt la [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="50b89-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="50b89-106">La méthode **Export** copie le contenu d’un [*magasin de certificats*](../secgloss/c-gly.md) ouvert dans une chaîne encodée.</span><span class="sxs-lookup"><span data-stu-id="50b89-106">The **Export** method copies the contents of an open [*certificate store*](../secgloss/c-gly.md) to an encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="50b89-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50b89-107">Syntax</span></span>


```VB
Store.Export( _
  [ ByVal SaveAs ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="50b89-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50b89-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50b89-109">*Enregistreras* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="50b89-109">*SaveAs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="50b89-110">Valeur de l’énumération de type de stockage de l' [ \_ \_ enregistrement \_ en tant \_ ](capicom-store-save-as-type.md) que, qui indique le format de l’opération d’exportation.</span><span class="sxs-lookup"><span data-stu-id="50b89-110">A value of the [CAPICOM\_STORE\_SAVE\_AS\_TYPE](capicom-store-save-as-type.md) enumeration that indicates the format for the export operation.</span></span> <span data-ttu-id="50b89-111">La valeur par défaut est CAPICOM \_ Store \_ Save \_ As \_ serialized.</span><span class="sxs-lookup"><span data-stu-id="50b89-111">The default value is CAPICOM\_STORE\_SAVE\_AS\_SERIALIZED.</span></span> <span data-ttu-id="50b89-112">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="50b89-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="50b89-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="50b89-113">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="50b89-114">Signification</span><span class="sxs-lookup"><span data-stu-id="50b89-114">Meaning</span></span>                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPICOM_STORE_SAVE_AS_SERIALIZED"></span><span id="capicom_store_save_as_serialized"></span><dl> <span data-ttu-id="50b89-115"><dt>**\_ \_ Enregistrer \_ en tant que stockage \_ sérialisé**</dt></span><span class="sxs-lookup"><span data-stu-id="50b89-115"><dt>**CAPICOM\_STORE\_SAVE\_AS\_SERIALIZED**</dt></span></span> </dl> | <span data-ttu-id="50b89-116">Le magasin est enregistré au format sérialisé.</span><span class="sxs-lookup"><span data-stu-id="50b89-116">The store is saved in serialized format.</span></span><br/> |
| <span id="CAPICOM_STORE_SAVE_AS_PKCS7"></span><span id="capicom_store_save_as_pkcs7"></span><dl> <span data-ttu-id="50b89-117"><dt>**\_ \_ Enregistrer \_ en tant que Registre \_ PKCS7**</dt></span><span class="sxs-lookup"><span data-stu-id="50b89-117"><dt>**CAPICOM\_STORE\_SAVE\_AS\_PKCS7**</dt></span></span> </dl>                | <span data-ttu-id="50b89-118">Le magasin est enregistré au \# format PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="50b89-118">The store is saved in PKCS \#7 format.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="50b89-119">*EncodingType* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="50b89-119">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="50b89-120">Valeur de l’énumération de [ \_ \_ type d’encodage](capicom-encoding-type.md) CAPICOM qui indique le type d’encodage du magasin exporté.</span><span class="sxs-lookup"><span data-stu-id="50b89-120">A value of the [CAPICOM\_ENCODING\_TYPE](capicom-encoding-type.md) enumeration that indicates the encoding type of the exported store.</span></span> <span data-ttu-id="50b89-121">La valeur par défaut est CAPICOM \_ encode \_ Base64.</span><span class="sxs-lookup"><span data-stu-id="50b89-121">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="50b89-122">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="50b89-122">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="50b89-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="50b89-123">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="50b89-124">Signification</span><span class="sxs-lookup"><span data-stu-id="50b89-124">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="50b89-125"><dt>**\_coder \_ tout**</dt></span><span class="sxs-lookup"><span data-stu-id="50b89-125"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="50b89-126">Ce type d’encodage est utilisé uniquement lorsque les données d’entrée ont un type d’encodage inconnu.</span><span class="sxs-lookup"><span data-stu-id="50b89-126">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="50b89-127">Si cette valeur est utilisée pour spécifier le type d’encodage de la sortie, CAPICOM est utilisé à la \_ \_ place.</span><span class="sxs-lookup"><span data-stu-id="50b89-127">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="50b89-128">Introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="50b89-128">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="50b89-129"><dt>**\_Encode \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="50b89-129"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="50b89-130">Les données sont enregistrées sous la forme d’une chaîne encodée en base64.</span><span class="sxs-lookup"><span data-stu-id="50b89-130">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="50b89-131"><dt>**codage d’un \_ \_ fichier binaire CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="50b89-131"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="50b89-132">Les données sont enregistrées sous la forme d’une séquence binaire pure.</span><span class="sxs-lookup"><span data-stu-id="50b89-132">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50b89-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="50b89-133">Return value</span></span>

<span data-ttu-id="50b89-134">Cette méthode retourne une chaîne qui contient les certificats dans le magasin dans le formulaire d’encodage spécifié.</span><span class="sxs-lookup"><span data-stu-id="50b89-134">This method returns a string that contains the certificates in the store in the specified encoding form.</span></span>

## <a name="requirements"></a><span data-ttu-id="50b89-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50b89-135">Requirements</span></span>



| <span data-ttu-id="50b89-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50b89-136">Requirement</span></span> | <span data-ttu-id="50b89-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="50b89-137">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="50b89-138">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="50b89-138">Redistributable</span></span><br/> | <span data-ttu-id="50b89-139">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="50b89-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="50b89-140">DLL</span><span class="sxs-lookup"><span data-stu-id="50b89-140">DLL</span></span><br/>             | <dl> <span data-ttu-id="50b89-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50b89-141"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50b89-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50b89-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50b89-143">**Magasin**</span><span class="sxs-lookup"><span data-stu-id="50b89-143">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="50b89-144">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="50b89-144">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
