---
description: Définit les codes d’erreur retournés par CAPICOM.
ms.assetid: e72b8290-b482-4629-8b87-5a15677865a6
title: Énumération CAPICOM_ERROR_CODE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ERROR_CODE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: ccd4963c83f1ad7ce3bc686b7736ce47d699ce30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537749"
---
# <a name="capicom_error_code-enumeration"></a><span data-ttu-id="97394-103">\_Énumération de code d’erreur CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="97394-103">CAPICOM\_ERROR\_CODE enumeration</span></span>

<span data-ttu-id="97394-104">Le type d’énumération du **\_ \_ code d’erreur CAPICOM** définit les codes d’erreur retournés par CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="97394-104">The **CAPICOM\_ERROR\_CODE** enumeration type defines error codes that are returned by CAPICOM.</span></span>

> [!Note]  
> <span data-ttu-id="97394-105">Visual Basic Scripting Edition Erreurs retournent une valeur **Err. Number** supérieure à zéro.</span><span class="sxs-lookup"><span data-stu-id="97394-105">Visual Basic Scripting Edition errors return an **Err.number** value greater than zero.</span></span> <span data-ttu-id="97394-106">Pour ces erreurs, les valeurs de **Err. Description** fournissent des informations sur la cause de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="97394-106">For those errors, **Err.Description** values provide information about the cause of the error.</span></span> <span data-ttu-id="97394-107">Outre les erreurs de Visual Basic Scripting Edition, les erreurs CAPICOM retournent les codes définis par le **\_ \_ code d’erreur CAPICOM**.</span><span class="sxs-lookup"><span data-stu-id="97394-107">In addition to Visual Basic Scripting Edition errors, CAPICOM errors return the codes defined by **CAPICOM\_ERROR\_CODE**.</span></span>

 

## <a name="members"></a><span data-ttu-id="97394-108">Membres</span><span class="sxs-lookup"><span data-stu-id="97394-108">Members</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="97394-109">Membre</span><span class="sxs-lookup"><span data-stu-id="97394-109">Member</span></span></th>
<th><span data-ttu-id="97394-110">Description</span><span class="sxs-lookup"><span data-stu-id="97394-110">Description</span></span></th>
<th><span data-ttu-id="97394-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="97394-111">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="97394-112"><strong>CAPICOM_E_ENCODE_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="97394-112"><strong>CAPICOM_E_ENCODE_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="97394-113">Un type d’encodage non valide a été utilisé.</span><span class="sxs-lookup"><span data-stu-id="97394-113">An encoding type that is not valid was used.</span></span><br/> <span data-ttu-id="97394-114">La liste suivante répertorie les types d’encodage valides :</span><span class="sxs-lookup"><span data-stu-id="97394-114">The following list shows the valid encoding types:</span></span>
<ul>
<li><span data-ttu-id="97394-115">CAPICOM_ENCODE_ANY</span><span class="sxs-lookup"><span data-stu-id="97394-115">CAPICOM_ENCODE_ANY</span></span></li>
<li><span data-ttu-id="97394-116">CAPICOM_ENCODE_BASE64</span><span class="sxs-lookup"><span data-stu-id="97394-116">CAPICOM_ENCODE_BASE64</span></span></li>
<li><span data-ttu-id="97394-117">CAPICOM_ENCODE_BINARY</span><span class="sxs-lookup"><span data-stu-id="97394-117">CAPICOM_ENCODE_BINARY</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="97394-118">0x80880100</span><span class="sxs-lookup"><span data-stu-id="97394-118">0x80880100</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97394-119"><strong>CAPICOM_E_EKU_INVALID_OID</strong></span><span class="sxs-lookup"><span data-stu-id="97394-119"><strong>CAPICOM_E_EKU_INVALID_OID</strong></span></span></td>
<td><span data-ttu-id="97394-120">La propriété <a href="eku-oid.md"><strong>OID</strong></a> de l’objet <a href="eku.md"><strong>EKU</strong></a> ne peut pas être définie, car la propriété <a href="eku-name.md"><strong>Name</strong></a> n’est pas définie sur CAPICOM_EKU_OTHER.</span><span class="sxs-lookup"><span data-stu-id="97394-120">The <a href="eku-oid.md"><strong>OID</strong></a> property of the <a href="eku.md"><strong>EKU</strong></a> object cannot be set because the <a href="eku-name.md"><strong>Name</strong></a> property is not set to CAPICOM_EKU_OTHER.</span></span><br/> <span data-ttu-id="97394-121">Définissez la propriété <a href="eku-name.md"><strong>nom</strong></a> sur CAPICOM_EKU_OTHER avant de définir la propriété <a href="eku-oid.md"><strong>OID</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="97394-121">Set the <a href="eku-name.md"><strong>Name</strong></a> property to CAPICOM_EKU_OTHER before setting the <a href="eku-oid.md"><strong>OID</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="97394-122">0x80880200</span><span class="sxs-lookup"><span data-stu-id="97394-122">0x80880200</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97394-123"><strong>CAPICOM_E_EKU_OID_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="97394-123"><strong>CAPICOM_E_EKU_OID_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="97394-124">La propriété <a href="eku-oid.md"><strong>OID</strong></a> de l’objet <a href="eku.md"><strong>EKU</strong></a> n’a pas été initialisée.</span><span class="sxs-lookup"><span data-stu-id="97394-124">The <a href="eku-oid.md"><strong>OID</strong></a> property of the <a href="eku.md"><strong>EKU</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="97394-125">Affectez à la propriété <a href="eku-name.md"><strong>Name</strong></a> une valeur autre que CAPICOM_EKU_OTHER, ou affectez à la propriété <strong>name</strong> la valeur CAPICOM_EKU_OTHER et à la propriété <a href="eku-oid.md"><strong>OID</strong></a> la valeur.</span><span class="sxs-lookup"><span data-stu-id="97394-125">Either set the <a href="eku-name.md"><strong>Name</strong></a> property to anything other than CAPICOM_EKU_OTHER, or set the <strong>Name</strong> property to CAPICOM_EKU_OTHER and the <a href="eku-oid.md"><strong>OID</strong></a> property to a value.</span></span><br/></td>
<td><span data-ttu-id="97394-126">0x80880201</span><span class="sxs-lookup"><span data-stu-id="97394-126">0x80880201</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97394-127"><strong>CAPICOM_E_CERTIFICATE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="97394-127"><strong>CAPICOM_E_CERTIFICATE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="97394-128">L’objet de <a href="certificate.md"><strong>certificat</strong></a> n’a pas été initialisé.</span><span class="sxs-lookup"><span data-stu-id="97394-128">The <a href="certificate.md"><strong>Certificate</strong></a> object has not been initialized.</span></span><br/> <span data-ttu-id="97394-129">En règle générale, ce code d’erreur est retourné lorsqu’un objet de <a href="certificate.md"><strong>certificat</strong></a> est instancié, mais n’est pas associé à un certificat numérique.</span><span class="sxs-lookup"><span data-stu-id="97394-129">Usually, this error code is returned when a <a href="certificate.md"><strong>Certificate</strong></a> object is instantiated but not associated with a digital certificate.</span></span> <span data-ttu-id="97394-130">Pour associer l’objet à un certificat numérique, affectez-le à un objet de <strong>certificat</strong> existant ou appelez la méthode <a href="certificate-import.md"><strong>Import</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="97394-130">To associate the object with a digital certificate, either assign it to an existing <strong>Certificate</strong> object or call the <a href="certificate-import.md"><strong>Import</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="97394-131">0x80880210</span><span class="sxs-lookup"><span data-stu-id="97394-131">0x80880210</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97394-132"><strong>CAPICOM_E_CERTIFICATE_NO_PRIVATE_KEY</strong></span><span class="sxs-lookup"><span data-stu-id="97394-132"><strong>CAPICOM_E_CERTIFICATE_NO_PRIVATE_KEY</strong></span></span></td>
<td><span data-ttu-id="97394-133">L’objet <a href="certificate.md"><strong>certificat</strong></a> n’a pas de clé privée associée.</span><span class="sxs-lookup"><span data-stu-id="97394-133">The <a href="certificate.md"><strong>Certificate</strong></a> object does not have an associated private key.</span></span><br/> <span data-ttu-id="97394-134">Ce code d’erreur est retourné lorsqu’une tentative est faite pour signer des données à l’aide de la clé privée du signataire, mais l’objet de <a href="certificate.md"><strong>certificat</strong></a> associé à l’objet <a href="signer.md"><strong>signataire</strong></a> ne peut pas être utilisé pour l’opération de signature.</span><span class="sxs-lookup"><span data-stu-id="97394-134">This error code is returned when an attempt is made to sign data using the signer's private key, but the <a href="certificate.md"><strong>Certificate</strong></a> object that is associated with the <a href="signer.md"><strong>Signer</strong></a> object cannot be used for the signing operation.</span></span><br/></td>
<td><span data-ttu-id="97394-135">0x80880211</span><span class="sxs-lookup"><span data-stu-id="97394-135">0x80880211</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97394-136"><strong>CAPICOM_E_CHAIN_NOT_BUILT</strong></span><span class="sxs-lookup"><span data-stu-id="97394-136"><strong>CAPICOM_E_CHAIN_NOT_BUILT</strong></span></span></td>
<td><span data-ttu-id="97394-137">L’objet de <a href="chain.md"><strong>chaîne</strong></a> n’a pas été initialisé.</span><span class="sxs-lookup"><span data-stu-id="97394-137">The <a href="chain.md"><strong>Chain</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="97394-138">Pour initialiser l’objet de <a href="chain.md"><strong>chaîne</strong></a> , appelez la méthode de <a href="chain-build.md"><strong>génération</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="97394-138">To initialize the <a href="chain.md"><strong>Chain</strong></a> object, call the <a href="chain-build.md"><strong>Build</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="97394-139">0x80880220</span><span class="sxs-lookup"><span data-stu-id="97394-139">0x80880220</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97394-140"><strong>CAPICOM_E_STORE_NOT_OPENED</strong></span><span class="sxs-lookup"><span data-stu-id="97394-140"><strong>CAPICOM_E_STORE_NOT_OPENED</strong></span></span></td>
<td><span data-ttu-id="97394-141">L’objet <a href="store.md"><strong>Store</strong></a> n’a pas été initialisé.</span><span class="sxs-lookup"><span data-stu-id="97394-141">The <a href="store.md"><strong>Store</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="97394-142">Pour initialiser l’objet <a href="store.md"><strong>Store</strong></a> , appelez la méthode <a href="store-open.md"><strong>Open</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="97394-142">To initialize the <a href="store.md"><strong>Store</strong></a> object, call the <a href="store-open.md"><strong>Open</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="97394-143">0x80880230</span><span class="sxs-lookup"><span data-stu-id="97394-143">0x80880230</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97394-144"><strong>CAPICOM_E_STORE_EMPTY</strong></span><span class="sxs-lookup"><span data-stu-id="97394-144"><strong>CAPICOM_E_STORE_EMPTY</strong></span></span></td>
<td><span data-ttu-id="97394-145">L’objet <a href="store.md"><strong>Store</strong></a> ne contient aucun objet de <a href="certificate.md"><strong>certificat</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="97394-145">The <a href="store.md"><strong>Store</strong></a> object does not contain any <a href="certificate.md"><strong>Certificate</strong></a> objects.</span></span><br/></td>
<td><span data-ttu-id="97394-146">0x80880231</span><span class="sxs-lookup"><span data-stu-id="97394-146">0x80880231</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97394-147"><strong>CAPICOM_E_STORE_INVALID_OPEN_MODE</strong></span><span class="sxs-lookup"><span data-stu-id="97394-147"><strong>CAPICOM_E_STORE_INVALID_OPEN_MODE</strong></span></span></td>
<td><span data-ttu-id="97394-148">Le paramètre <em>OpenMode</em> de la méthode <a href="store-open.md"><strong>Store. Open</strong></a> ne contient pas de valeur valide de CAPICOM_STORE_OPEN_MODE.</span><span class="sxs-lookup"><span data-stu-id="97394-148">The <em>OpenMode</em> parameter of the <a href="store-open.md"><strong>Store.Open</strong></a> method does not contain a valid value of CAPICOM_STORE_OPEN_MODE.</span></span><br/> <span data-ttu-id="97394-149">La liste suivante indique les valeurs valides de CAPICOM_STORE_OPEN_MODE :</span><span class="sxs-lookup"><span data-stu-id="97394-149">The following list shows the valid values of CAPICOM_STORE_OPEN_MODE:</span></span>
<ul>
<li><span data-ttu-id="97394-150">CAPICOM_STORE_OPEN_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="97394-150">CAPICOM_STORE_OPEN_READ_ONLY</span></span></li>
<li><span data-ttu-id="97394-151">CAPICOM_STORE_OPEN_READ_WRITE</span><span class="sxs-lookup"><span data-stu-id="97394-151">CAPICOM_STORE_OPEN_READ_WRITE</span></span></li>
<li><span data-ttu-id="97394-152">CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="97394-152">CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED</span></span></li>
<li><span data-ttu-id="97394-153">CAPICOM_STORE_OPEN_EXISTING_ONLY</span><span class="sxs-lookup"><span data-stu-id="97394-153">CAPICOM_STORE_OPEN_EXISTING_ONLY</span></span></li>
<li><span data-ttu-id="97394-154">CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED</span><span class="sxs-lookup"><span data-stu-id="97394-154">CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="97394-155">0x80880232</span><span class="sxs-lookup"><span data-stu-id="97394-155">0x80880232</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97394-156"><strong>CAPICOM_E_STORE_INVALID_SAVE_AS_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="97394-156"><strong>CAPICOM_E_STORE_INVALID_SAVE_AS_TYPE</strong></span></span></td>
<td><span data-ttu-id="97394-157">La valeur <em>SaveAs</em> transmise à la méthode d' <a href="store-export.md"><strong>exportation</strong></a> de l’objet <a href="store.md"><strong>Store</strong></a> n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="97394-157">The <em>SaveAs</em> value passed to the <a href="store-export.md"><strong>Export</strong></a> method of the <a href="store.md"><strong>Store</strong></a> object was not valid.</span></span> <br/> <span data-ttu-id="97394-158">La liste suivante affiche les valeurs <em>SaveAs</em> valides :</span><span class="sxs-lookup"><span data-stu-id="97394-158">The following list shows the valid <em>SaveAs</em> values:</span></span>
<ul>
<li><span data-ttu-id="97394-159">CAPICOM_STORE_SAVE_AS_SERIALIZED</span><span class="sxs-lookup"><span data-stu-id="97394-159">CAPICOM_STORE_SAVE_AS_SERIALIZED</span></span></li>
<li><span data-ttu-id="97394-160">CAPICOM_STORE_SAVE_AS_PKCS7</span><span class="sxs-lookup"><span data-stu-id="97394-160">CAPICOM_STORE_SAVE_AS_PKCS7</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="97394-161">0x80880233</span><span class="sxs-lookup"><span data-stu-id="97394-161">0x80880233</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97394-162"><strong>CAPICOM_E_ATTRIBUTE_NAME_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="97394-162"><strong>CAPICOM_E_ATTRIBUTE_NAME_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="97394-163">La propriété de <a href="attribute-name.md"><strong>nom</strong></a> de l’objet d' <a href="attribute.md"><strong>attribut</strong></a> n’a pas été initialisée.</span><span class="sxs-lookup"><span data-stu-id="97394-163">The <a href="attribute-name.md"><strong>Name</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="97394-164">Définissez la propriété <a href="attribute-name.md"><strong>Name</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="97394-164">Set the <a href="attribute-name.md"><strong>Name</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="97394-165">0x80880240</span><span class="sxs-lookup"><span data-stu-id="97394-165">0x80880240</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97394-166"><strong>CAPICOM_E_ATTRIBUTE_VALUE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="97394-166"><strong>CAPICOM_E_ATTRIBUTE_VALUE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="97394-167">La propriété <a href="attribute-value.md"><strong>value</strong></a> de l’objet <a href="attribute.md"><strong>attribut</strong></a> n’a pas été initialisée.</span><span class="sxs-lookup"><span data-stu-id="97394-167">The <a href="attribute-value.md"><strong>Value</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="97394-168">Définissez la propriété <a href="attribute-value.md"><strong>value</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="97394-168">Set the <a href="attribute-value.md"><strong>Value</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="97394-169">0x80880241</span><span class="sxs-lookup"><span data-stu-id="97394-169">0x80880241</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97394-170"><strong>CAPICOM_E_ATTRIBUTE_INVALID_NAME</strong></span><span class="sxs-lookup"><span data-stu-id="97394-170"><strong>CAPICOM_E_ATTRIBUTE_INVALID_NAME</strong></span></span></td>
<td><span data-ttu-id="97394-171">La propriété de <a href="attribute-name.md"><strong>nom</strong></a> de l’objet d' <a href="attribute.md"><strong>attribut</strong></a> n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="97394-171">The <a href="attribute-name.md"><strong>Name</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object is not valid.</span></span> <br/> <span data-ttu-id="97394-172">La liste suivante répertorie les noms d’attributs valides :</span><span class="sxs-lookup"><span data-stu-id="97394-172">The following list shows the valid attribute names:</span></span>
<ul>
<li><span data-ttu-id="97394-173">CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME</span><span class="sxs-lookup"><span data-stu-id="97394-173">CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME</span></span></li>
<li><span data-ttu-id="97394-174">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME</span><span class="sxs-lookup"><span data-stu-id="97394-174">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME</span></span></li>
<li><span data-ttu-id="97394-175">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="97394-175">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="97394-176">0x80880242</span><span class="sxs-lookup"><span data-stu-id="97394-176">0x80880242</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97394-177"><strong>CAPICOM_E_ATTRIBUTE_INVALID_VALUE</strong></span><span class="sxs-lookup"><span data-stu-id="97394-177"><strong>CAPICOM_E_ATTRIBUTE_INVALID_VALUE</strong></span></span></td>
<td><span data-ttu-id="97394-178">La propriété <a href="attribute-value.md"><strong>value</strong></a> de l’objet <a href="attribute.md"><strong>attribut</strong></a> n’est pas valide, car le type de données ne correspond pas au type de données indiqué par la propriété <strong>Name</strong> .</span><span class="sxs-lookup"><span data-stu-id="97394-178">The <a href="attribute-value.md"><strong>Value</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object is not valid because the data type does not match the data type indicated by the <strong>Name</strong> property.</span></span> <br/> <span data-ttu-id="97394-179">Par exemple, si la propriété <a href="attribute-value.md"><strong>Name</strong></a> est définie sur CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME, le type de données doit être <strong>Date</strong>.</span><span class="sxs-lookup"><span data-stu-id="97394-179">For example, if the <a href="attribute-value.md"><strong>Name</strong></a> property is set to CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME, the data type must be <strong>DATE</strong>.</span></span><br/></td>
<td><span data-ttu-id="97394-180">0x80880243</span><span class="sxs-lookup"><span data-stu-id="97394-180">0x80880243</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97394-181"><strong>CAPICOM_E_SIGNER_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="97394-181"><strong>CAPICOM_E_SIGNER_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="97394-182">L’objet <a href="signer.md"><strong>signataire</strong></a> n’a pas été initialisé.</span><span class="sxs-lookup"><span data-stu-id="97394-182">The <a href="signer.md"><strong>Signer</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="97394-183">Pour initialiser l’objet <a href="signer.md"><strong>signataire</strong></a> , définissez la propriété <a href="signer-certificate.md"><strong>certificat</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="97394-183">To initialize the <a href="signer.md"><strong>Signer</strong></a> object, set the <a href="signer-certificate.md"><strong>Certificate</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="97394-184">0x80880250</span><span class="sxs-lookup"><span data-stu-id="97394-184">0x80880250</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97394-185"><strong>CAPICOM_E_SIGNER_NOT_FOUND</strong></span><span class="sxs-lookup"><span data-stu-id="97394-185"><strong>CAPICOM_E_SIGNER_NOT_FOUND</strong></span></span></td>
<td><span data-ttu-id="97394-186">Le signataire est introuvable dans l’objet <a href="signeddata.md"><strong>SignedData</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="97394-186">The signer cannot be found in the <a href="signeddata.md"><strong>SignedData</strong></a> object.</span></span> <br/> <span data-ttu-id="97394-187">En règle générale, cela ne se produit pas avec un objet <a href="signeddata.md"><strong>SignedData</strong></a> qui a été créé par CAPICOM ; Toutefois, si l’objet <strong>SignedData</strong> a été créé par un produit tiers, le certificat du signataire peut ne pas être inclus dans la structure de #7 Pkcs.</span><span class="sxs-lookup"><span data-stu-id="97394-187">Usually, this does not happen with a <a href="signeddata.md"><strong>SignedData</strong></a> object that was created by CAPICOM; however, if the <strong>SignedData</strong> object was created by a third-party product, the signer's certificate may not be included in the PKCS #7 structure.</span></span><br/></td>
<td><span data-ttu-id="97394-188">0x80880251</span><span class="sxs-lookup"><span data-stu-id="97394-188">0x80880251</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97394-189"><strong>CAPICOM_E_SIGNER_NO_CHAIN</strong></span><span class="sxs-lookup"><span data-stu-id="97394-189"><strong>CAPICOM_E_SIGNER_NO_CHAIN</strong></span></span></td>
<td><span data-ttu-id="97394-190">Un objet <a href="chain.md"><strong>chaîne</strong></a> est introuvable dans l’objet <a href="signer.md"><strong>signataire</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="97394-190">A <a href="chain.md"><strong>Chain</strong></a> object cannot be found in the <a href="signer.md"><strong>Signer</strong></a> object.</span></span><br/></td>
<td><span data-ttu-id="97394-191">0x80880252//v 2.0</span><span class="sxs-lookup"><span data-stu-id="97394-191">0x80880252 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97394-192"><strong>CAPICOM_E_SIGNER_INVALID_USAGE</strong></span><span class="sxs-lookup"><span data-stu-id="97394-192"><strong>CAPICOM_E_SIGNER_INVALID_USAGE</strong></span></span></td>
<td><span data-ttu-id="97394-193">Une tentative d’utilisation du signataire est effectuée de manière non valide.</span><span class="sxs-lookup"><span data-stu-id="97394-193">An attempt is made to use the signer in a way that is not valid.</span></span><br/></td>
<td><span data-ttu-id="97394-194">0x80880253.//v2.0</span><span class="sxs-lookup"><span data-stu-id="97394-194">0x80880253 //v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97394-195"><strong>CAPICOM_E_SIGN_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="97394-195"><strong>CAPICOM_E_SIGN_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="97394-196">L’objet <a href="signeddata.md"><strong>SignedData</strong></a> n’a pas été initialisé.</span><span class="sxs-lookup"><span data-stu-id="97394-196">The <a href="signeddata.md"><strong>SignedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="97394-197">Pour initialiser l’objet <a href="signeddata.md"><strong>SignedData</strong></a> , définissez la propriété <a href="signeddata-content.md"><strong>content</strong></a> ou appelez la méthode <a href="signeddata-verify.md"><strong>verify</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="97394-197">To initialize the <a href="signeddata.md"><strong>SignedData</strong></a> object, set the <a href="signeddata-content.md"><strong>Content</strong></a> property or call the <a href="signeddata-verify.md"><strong>Verify</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="97394-198">0x80880260</span><span class="sxs-lookup"><span data-stu-id="97394-198">0x80880260</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97394-199"><strong>CAPICOM_E_SIGN_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="97394-199"><strong>CAPICOM_E_SIGN_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="97394-200">L’objet <a href="signeddata.md"><strong>SignedData</strong></a> contient un type qui n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="97394-200">The <a href="signeddata.md"><strong>SignedData</strong></a> object contains a type that is not valid.</span></span> <br/> <span data-ttu-id="97394-201">En règle générale, cela se produit lorsqu’une tentative est effectuée pour vérifier un message enveloppé avec un objet <a href="signeddata.md"><strong>SignedData</strong></a> ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="97394-201">Usually, this happens when an attempt is made to verify an enveloped message with a <a href="signeddata.md"><strong>SignedData</strong></a> object or vice versa.</span></span><br/></td>
<td><span data-ttu-id="97394-202">0x80880261</span><span class="sxs-lookup"><span data-stu-id="97394-202">0x80880261</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97394-203"><strong>CAPICOM_E_SIGN_NOT_SIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="97394-203"><strong>CAPICOM_E_SIGN_NOT_SIGNED</strong></span></span></td>
<td><span data-ttu-id="97394-204">L’objet <a href="signeddata.md"><strong>SignedData</strong></a> n’a pas été signé.</span><span class="sxs-lookup"><span data-stu-id="97394-204">The <a href="signeddata.md"><strong>SignedData</strong></a> object has not been signed.</span></span> <br/> <span data-ttu-id="97394-205">Pour signer l’objet <a href="signeddata.md"><strong>SignedData</strong></a> , appelez la méthode <a href="signeddata-sign.md"><strong>Sign</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="97394-205">To sign the <a href="signeddata.md"><strong>SignedData</strong></a> object, call the <a href="signeddata-sign.md"><strong>Sign</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="97394-206">0x80880262</span><span class="sxs-lookup"><span data-stu-id="97394-206">0x80880262</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97394-207"><strong>CAPICOM_E_INVALID_ALGORITHM</strong></span><span class="sxs-lookup"><span data-stu-id="97394-207"><strong>CAPICOM_E_INVALID_ALGORITHM</strong></span></span></td>
<td><span data-ttu-id="97394-208">La valeur de l’algorithme pour la propriété <a href="algorithm-name.md"><strong>Name</strong></a> de l’objet <a href="algorithm.md"><strong>algorithme</strong></a> n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="97394-208">The algorithm value for the <a href="algorithm-name.md"><strong>Name</strong></a> property of the <a href="algorithm.md"><strong>Algorithm</strong></a> object is not valid.</span></span> <br/> <span data-ttu-id="97394-209">La liste suivante indique les valeurs d’algorithme valides pour la propriété <a href="algorithm-name.md"><strong>Name</strong></a> :</span><span class="sxs-lookup"><span data-stu-id="97394-209">The following list shows the valid algorithm values for the <a href="algorithm-name.md"><strong>Name</strong></a> property:</span></span>
<ul>
<li><span data-ttu-id="97394-210">CAPICOM_ENCRYPTION_ALGORITHM_RC2</span><span class="sxs-lookup"><span data-stu-id="97394-210">CAPICOM_ENCRYPTION_ALGORITHM_RC2</span></span></li>
<li><span data-ttu-id="97394-211">CAPICOM_ENCRYPTION_ALGORITHM_RC4</span><span class="sxs-lookup"><span data-stu-id="97394-211">CAPICOM_ENCRYPTION_ALGORITHM_RC4</span></span></li>
<li><span data-ttu-id="97394-212">CAPICOM_ENCRYPTION_ALGORITHM_DES</span><span class="sxs-lookup"><span data-stu-id="97394-212">CAPICOM_ENCRYPTION_ALGORITHM_DES</span></span></li>
<li><span data-ttu-id="97394-213">CAPICOM_ENCRYPTION_ALGORITHM_3DES</span><span class="sxs-lookup"><span data-stu-id="97394-213">CAPICOM_ENCRYPTION_ALGORITHM_3DES</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="97394-214">0x80880270</span><span class="sxs-lookup"><span data-stu-id="97394-214">0x80880270</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97394-215"><strong>CAPICOM_E_INVALID_KEY_LENGTH</strong></span><span class="sxs-lookup"><span data-stu-id="97394-215"><strong>CAPICOM_E_INVALID_KEY_LENGTH</strong></span></span></td>
<td><span data-ttu-id="97394-216">La valeur de la longueur de clé de la propriété <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> de l’objet <a href="algorithm.md"><strong>algorithme</strong></a> n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="97394-216">The key length value for the <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> property of the <a href="algorithm.md"><strong>Algorithm</strong></a> object is not valid.</span></span> <br/> <span data-ttu-id="97394-217">La liste suivante indique les valeurs de longueur de clé valides pour la propriété <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> :</span><span class="sxs-lookup"><span data-stu-id="97394-217">The following list shows the valid key length values for the <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> property:</span></span>
<ul>
<li><span data-ttu-id="97394-218">CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM</span><span class="sxs-lookup"><span data-stu-id="97394-218">CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM</span></span></li>
<li><span data-ttu-id="97394-219">CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS</span><span class="sxs-lookup"><span data-stu-id="97394-219">CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS</span></span></li>
<li><span data-ttu-id="97394-220">CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS</span><span class="sxs-lookup"><span data-stu-id="97394-220">CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS</span></span></li>
<li><span data-ttu-id="97394-221">CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS</span><span class="sxs-lookup"><span data-stu-id="97394-221">CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="97394-222">0x80880271</span><span class="sxs-lookup"><span data-stu-id="97394-222">0x80880271</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97394-223"><strong>CAPICOM_E_ENVELOP_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="97394-223"><strong>CAPICOM_E_ENVELOP_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="97394-224">L’objet <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> n’a pas été initialisé.</span><span class="sxs-lookup"><span data-stu-id="97394-224">The <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="97394-225">Pour initialiser l’objet <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> , définissez la propriété <a href="envelopeddata-content.md"><strong>content</strong></a> ou appelez la méthode <a href="envelopeddata-decrypt.md"><strong>Decrypt</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="97394-225">To initialize the <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object, either set the <a href="envelopeddata-content.md"><strong>Content</strong></a> property or call the <a href="envelopeddata-decrypt.md"><strong>Decrypt</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="97394-226">0x80880280</span><span class="sxs-lookup"><span data-stu-id="97394-226">0x80880280</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97394-227"><strong>CAPICOM_E_ENVELOP_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="97394-227"><strong>CAPICOM_E_ENVELOP_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="97394-228">L’objet <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> contient un type qui n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="97394-228">The <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object contains a type that is not valid.</span></span> <br/> <span data-ttu-id="97394-229">En règle générale, cela se produit lorsqu’une tentative est effectuée pour vérifier un message signé avec un objet <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="97394-229">Usually, this happens when an attempt is made to verify a signed message with an <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object or vice versa.</span></span><br/></td>
<td><span data-ttu-id="97394-230">0x80880281</span><span class="sxs-lookup"><span data-stu-id="97394-230">0x80880281</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97394-231"><strong>CAPICOM_E_ENVELOP_NO_RECIPIENT</strong></span><span class="sxs-lookup"><span data-stu-id="97394-231"><strong>CAPICOM_E_ENVELOP_NO_RECIPIENT</strong></span></span></td>
<td><span data-ttu-id="97394-232">Aucun destinataire n’est spécifié dans l’objet <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> lorsque la méthode <a href="envelopeddata-encrypt.md"><strong>Encrypt</strong></a> d’un objet <strong>EnvelopedData</strong> est appelée.</span><span class="sxs-lookup"><span data-stu-id="97394-232">There is no recipient specified in the <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object when the <a href="envelopeddata-encrypt.md"><strong>Encrypt</strong></a> method of an <strong>EnvelopedData</strong> object is called.</span></span> <br/> <span data-ttu-id="97394-233">Pour ajouter un destinataire, appelez la méthode <a href="recipients-add.md"><strong>Recipients. Add</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="97394-233">To add a recipient, call the <a href="recipients-add.md"><strong>Recipients.Add</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="97394-234">0x80880282</span><span class="sxs-lookup"><span data-stu-id="97394-234">0x80880282</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97394-235"><strong>CAPICOM_E_ENVELOP_RECIPIENT_NOT_FOUND</strong></span><span class="sxs-lookup"><span data-stu-id="97394-235"><strong>CAPICOM_E_ENVELOP_RECIPIENT_NOT_FOUND</strong></span></span></td>
<td><span data-ttu-id="97394-236">Le destinataire est introuvable dans l’objet <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="97394-236">The recipient cannot be found in the <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object.</span></span> <br/> <span data-ttu-id="97394-237">En règle générale, cela ne se produit pas avec un objet <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> qui a été créé par CAPICOM ; Toutefois, si l’objet <strong>EnvelopedData</strong> a été créé par un produit tiers, le certificat du destinataire peut ne pas être inclus dans la structure de #7 Pkcs.</span><span class="sxs-lookup"><span data-stu-id="97394-237">Usually, this does not happen with an <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object that was created by CAPICOM; however, if the <strong>EnvelopedData</strong> object was created by a third-party product, the recipient's certificate may not be included in the PKCS #7 structure.</span></span><br/></td>
<td><span data-ttu-id="97394-238">0x80880283</span><span class="sxs-lookup"><span data-stu-id="97394-238">0x80880283</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97394-239"><strong>CAPICOM_E_ENCRYPT_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="97394-239"><strong>CAPICOM_E_ENCRYPT_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="97394-240">L’objet <a href="encrypteddata.md"><strong>EncryptedData</strong></a> n’a pas été initialisé.</span><span class="sxs-lookup"><span data-stu-id="97394-240">The <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="97394-241">Pour initialiser l’objet <a href="encrypteddata.md"><strong>EncryptedData</strong></a> , définissez la propriété de <a href="encrypteddata-content.md"><strong>contenu</strong></a> ou appelez la méthode <a href="encrypteddata-decrypt.md"><strong>Decrypt</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="97394-241">To initialize the <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object, either set the <a href="encrypteddata-content.md"><strong>Content</strong></a> property or call the <a href="encrypteddata-decrypt.md"><strong>Decrypt</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="97394-242">0x80880290</span><span class="sxs-lookup"><span data-stu-id="97394-242">0x80880290</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97394-243"><strong>CAPICOM_E_ENCRYPT_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="97394-243"><strong>CAPICOM_E_ENCRYPT_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="97394-244">L’objet <a href="encrypteddata.md"><strong>EncryptedData</strong></a> n’est pas un type valide.</span><span class="sxs-lookup"><span data-stu-id="97394-244">The <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object is not a valid type.</span></span> <br/> <span data-ttu-id="97394-245">En règle générale, cela signifie que les données sont endommagées.</span><span class="sxs-lookup"><span data-stu-id="97394-245">Usually, this means the data is corrupted.</span></span><br/></td>
<td><span data-ttu-id="97394-246">0x80880291</span><span class="sxs-lookup"><span data-stu-id="97394-246">0x80880291</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97394-247"><strong>CAPICOM_E_ENCRYPT_NO_SECRET</strong></span><span class="sxs-lookup"><span data-stu-id="97394-247"><strong>CAPICOM_E_ENCRYPT_NO_SECRET</strong></span></span></td>
<td><span data-ttu-id="97394-248">Le secret d’un objet <a href="encrypteddata.md"><strong>EncryptedData</strong></a> n’a pas été initialisé.</span><span class="sxs-lookup"><span data-stu-id="97394-248">The secret of an <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="97394-249">Pour initialiser le secret d’un objet <a href="encrypteddata.md"><strong>EncryptedData</strong></a> , appelez la méthode <a href="encrypteddata-setsecret.md"><strong>SetSecret</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="97394-249">To initialize the secret of an <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object, call the <a href="encrypteddata-setsecret.md"><strong>SetSecret</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="97394-250">0x80880292</span><span class="sxs-lookup"><span data-stu-id="97394-250">0x80880292</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97394-251"><strong>CAPICOM_E_PRIVATE_KEY_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="97394-251"><strong>CAPICOM_E_PRIVATE_KEY_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="97394-252">L’objet <a href="privatekey.md"><strong>PrivateKey</strong></a> n’a pas été initialisé.</span><span class="sxs-lookup"><span data-stu-id="97394-252">The <a href="privatekey.md"><strong>PrivateKey</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="97394-253">0x80880300//v 2.0</span><span class="sxs-lookup"><span data-stu-id="97394-253">0x80880300 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97394-254"><strong>CAPICOM_E_PRIVATE_KEY_NOT_EXPORTABLE</strong></span><span class="sxs-lookup"><span data-stu-id="97394-254"><strong>CAPICOM_E_PRIVATE_KEY_NOT_EXPORTABLE</strong></span></span></td>
<td><span data-ttu-id="97394-255">Impossible d’exporter l’objet <a href="privatekey.md"><strong>PrivateKey</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="97394-255">The <a href="privatekey.md"><strong>PrivateKey</strong></a> object cannot be exported.</span></span><br/></td>
<td><span data-ttu-id="97394-256">0x80880301//v 2.0</span><span class="sxs-lookup"><span data-stu-id="97394-256">0x80880301 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97394-257"><strong>CAPICOM_E_ENCODE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="97394-257"><strong>CAPICOM_E_ENCODE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="97394-258">L’objet <a href="encodeddata.md"><strong>EncodedData</strong></a> n’a pas été initialisé.</span><span class="sxs-lookup"><span data-stu-id="97394-258">The <a href="encodeddata.md"><strong>EncodedData</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="97394-259">0x80880320//v 2.0</span><span class="sxs-lookup"><span data-stu-id="97394-259">0x80880320 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97394-260"><strong>CAPICOM_E_EXTENSION_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="97394-260"><strong>CAPICOM_E_EXTENSION_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="97394-261">L’objet d' <a href="extension.md"><strong>extension</strong></a> n’a pas été initialisé.</span><span class="sxs-lookup"><span data-stu-id="97394-261">The <a href="extension.md"><strong>Extension</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="97394-262">0x80880330//v 2.0</span><span class="sxs-lookup"><span data-stu-id="97394-262">0x80880330 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97394-263"><strong>CAPICOM_E_PROPERTY_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="97394-263"><strong>CAPICOM_E_PROPERTY_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="97394-264">La propriété <a href="extendedproperty-propid.md"><strong>propid</strong></a> de l’objet <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> n’a pas été initialisée.</span><span class="sxs-lookup"><span data-stu-id="97394-264">The <a href="extendedproperty-propid.md"><strong>PropID</strong></a> property of the <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="97394-265">0x80880340//v 2.0</span><span class="sxs-lookup"><span data-stu-id="97394-265">0x80880340 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97394-266"><strong>CAPICOM_E_FIND_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="97394-266"><strong>CAPICOM_E_FIND_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="97394-267">Le paramètre <em>FindType</em> de la méthode <a href="certificates-find.md"><strong>Certificates. Find</strong></a> n’est pas une valeur de l’énumération <a href="capicom-certificate-find-type.md"><strong>CAPICOM_CERTIFICATE_FIND_TYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="97394-267">The <em>FindType</em> parameter of the <a href="certificates-find.md"><strong>Certificates.Find</strong></a> method is not a value of the <a href="capicom-certificate-find-type.md"><strong>CAPICOM_CERTIFICATE_FIND_TYPE</strong></a> enumeration.</span></span><br/></td>
<td><span data-ttu-id="97394-268">0x80880350//v 2.0</span><span class="sxs-lookup"><span data-stu-id="97394-268">0x80880350 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97394-269"><strong>CAPICOM_E_FIND_INVALID_PREDEFINED_POLICY</strong></span><span class="sxs-lookup"><span data-stu-id="97394-269"><strong>CAPICOM_E_FIND_INVALID_PREDEFINED_POLICY</strong></span></span></td>
<td><span data-ttu-id="97394-270">La stratégie prédéfinie spécifiée pour l’opération de recherche n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="97394-270">The specified predefined policy for the find operation is not valid.</span></span><br/></td>
<td><span data-ttu-id="97394-271">0x80880351//v 2.0</span><span class="sxs-lookup"><span data-stu-id="97394-271">0x80880351 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97394-272"><strong>CAPICOM_E_CODE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="97394-272"><strong>CAPICOM_E_CODE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="97394-273">L’objet <a href="signedcode.md"><strong>SignedCode</strong></a> n’a pas été initialisé.</span><span class="sxs-lookup"><span data-stu-id="97394-273">The <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="97394-274">0x80880360//v 2.0</span><span class="sxs-lookup"><span data-stu-id="97394-274">0x80880360 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97394-275"><strong>CAPICOM_E_CODE_NOT_SIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="97394-275"><strong>CAPICOM_E_CODE_NOT_SIGNED</strong></span></span></td>
<td><span data-ttu-id="97394-276">L’objet <a href="signedcode.md"><strong>SignedCode</strong></a> n’a pas été signé.</span><span class="sxs-lookup"><span data-stu-id="97394-276">The <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been signed.</span></span><br/> <span data-ttu-id="97394-277">Pour signer l’objet <a href="signedcode.md"><strong>SignedCode</strong></a> , appelez la méthode <a href="signedcode-sign.md"><strong>Sign</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="97394-277">To sign the <a href="signedcode.md"><strong>SignedCode</strong></a> object, call the <a href="signedcode-sign.md"><strong>Sign</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="97394-278">0x80880361//v 2.0</span><span class="sxs-lookup"><span data-stu-id="97394-278">0x80880361 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97394-279"><strong>CAPICOM_E_CODE_DESCRIPTION_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="97394-279"><strong>CAPICOM_E_CODE_DESCRIPTION_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="97394-280">La propriété <a href="signedcode-description.md"><strong>Description</strong></a> de l’objet <a href="signedcode.md"><strong>SignedCode</strong></a> n’a pas été initialisée.</span><span class="sxs-lookup"><span data-stu-id="97394-280">The <a href="signedcode-description.md"><strong>Description</strong></a> property of the <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="97394-281">0x80880362//v 2.0</span><span class="sxs-lookup"><span data-stu-id="97394-281">0x80880362 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97394-282"><strong>CAPICOM_E_CODE_DESCRIPTION_URL_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="97394-282"><strong>CAPICOM_E_CODE_DESCRIPTION_URL_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="97394-283">La propriété <a href="signedcode-descriptionurl.md"><strong>DescriptionURL</strong></a> de l’objet <a href="signedcode.md"><strong>SignedCode</strong></a> n’a pas été initialisée.</span><span class="sxs-lookup"><span data-stu-id="97394-283">The <a href="signedcode-descriptionurl.md"><strong>DescriptionURL</strong></a> property of the <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="97394-284">0x80880363//v 2.0</span><span class="sxs-lookup"><span data-stu-id="97394-284">0x80880363 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97394-285"><strong>CAPICOM_E_CODE_INVALID_TIMESTAMP_URL</strong></span><span class="sxs-lookup"><span data-stu-id="97394-285"><strong>CAPICOM_E_CODE_INVALID_TIMESTAMP_URL</strong></span></span></td>
<td><span data-ttu-id="97394-286">Le paramètre d' <em>URL</em> de la méthode <a href="signedcode-timestamp.md"><strong>SignedCode. Timestamp</strong></a> n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="97394-286">The <em>URL</em> parameter of the <a href="signedcode-timestamp.md"><strong>SignedCode.Timestamp</strong></a> method is not valid.</span></span><br/></td>
<td><span data-ttu-id="97394-287">0x80880364//v 2.0</span><span class="sxs-lookup"><span data-stu-id="97394-287">0x80880364 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97394-288"><strong>CAPICOM_E_HASH_NO_DATA</strong></span><span class="sxs-lookup"><span data-stu-id="97394-288"><strong>CAPICOM_E_HASH_NO_DATA</strong></span></span></td>
<td><span data-ttu-id="97394-289">L’objet <a href="hasheddata.md"><strong>HashedData</strong></a> ne contient aucune donnée.</span><span class="sxs-lookup"><span data-stu-id="97394-289">The <a href="hasheddata.md"><strong>HashedData</strong></a> object does not contain any data.</span></span><br/></td>
<td><span data-ttu-id="97394-290">0x80880370//v 2.0</span><span class="sxs-lookup"><span data-stu-id="97394-290">0x80880370 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97394-291"><strong>CAPICOM_E_INVALID_CONVERT_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="97394-291"><strong>CAPICOM_E_INVALID_CONVERT_TYPE</strong></span></span></td>
<td><span data-ttu-id="97394-292">Le type de conversion n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="97394-292">The convert type is not valid.</span></span><br/></td>
<td><span data-ttu-id="97394-293">0x80880380//v 2.0</span><span class="sxs-lookup"><span data-stu-id="97394-293">0x80880380 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97394-294"><strong>CAPICOM_E_NOT_SUPPORTED</strong></span><span class="sxs-lookup"><span data-stu-id="97394-294"><strong>CAPICOM_E_NOT_SUPPORTED</strong></span></span></td>
<td><span data-ttu-id="97394-295">L’opération demandée n’est pas prise en charge dans la plateforme actuelle.</span><span class="sxs-lookup"><span data-stu-id="97394-295">The requested operation is not supported in the current platform.</span></span> <br/></td>
<td><span data-ttu-id="97394-296">0x80880900</span><span class="sxs-lookup"><span data-stu-id="97394-296">0x80880900</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97394-297"><strong>CAPICOM_E_UI_DISABLED</strong></span><span class="sxs-lookup"><span data-stu-id="97394-297"><strong>CAPICOM_E_UI_DISABLED</strong></span></span></td>
<td><span data-ttu-id="97394-298">Lors de la signature, la propriété <a href="signer-certificate.md"><strong>Certificate</strong></a> de l’objet <a href="signer.md"><strong>signataire</strong></a> n’a pas été définie, mais l’invite du certificat utilisateur a été désactivée.</span><span class="sxs-lookup"><span data-stu-id="97394-298">When signing, the <a href="signer-certificate.md"><strong>Certificate</strong></a> property of the <a href="signer.md"><strong>Signer</strong></a> object has not been set, but the prompt for the user certificate has been disabled.</span></span> <br/> <span data-ttu-id="97394-299">Activez l’invite en définissant la propriété <a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a> de l’objet de <a href="settings.md"><strong>paramètres</strong></a> , ou définissez la propriété <a href="signer-certificate.md"><strong>certificat</strong></a> de l’objet <a href="signer.md"><strong>signataire</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="97394-299">Either enable the prompt by setting the <a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a> property of the <a href="settings.md"><strong>Settings</strong></a> object, or set the <a href="signer-certificate.md"><strong>Certificate</strong></a> property of the <a href="signer.md"><strong>Signer</strong></a> object.</span></span><br/></td>
<td><span data-ttu-id="97394-300">0x80880901</span><span class="sxs-lookup"><span data-stu-id="97394-300">0x80880901</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97394-301"><strong>CAPICOM_E_CANCELLED</strong></span><span class="sxs-lookup"><span data-stu-id="97394-301"><strong>CAPICOM_E_CANCELLED</strong></span></span></td>
<td><span data-ttu-id="97394-302">L’opération a été annulée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="97394-302">The operation has been canceled by the user.</span></span> <br/> <span data-ttu-id="97394-303">Cela se produit lorsque l’utilisateur est invité à autoriser l’exécution d’une certaine opération, par exemple l’accès à la clé privée, et que l’utilisateur annule l’opération.</span><span class="sxs-lookup"><span data-stu-id="97394-303">This happens when the user is prompted for permission to carry out a certain operation, such as accessing the private key, and the user cancels the operation.</span></span><br/></td>
<td><span data-ttu-id="97394-304">0x80880902</span><span class="sxs-lookup"><span data-stu-id="97394-304">0x80880902</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97394-305"><strong>CAPICOM_E_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="97394-305"><strong>CAPICOM_E_NOT_ALLOWED</strong></span></span></td>
<td><span data-ttu-id="97394-306">L’opération tentée n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="97394-306">The attempted operation is not allowed.</span></span><br/> <span data-ttu-id="97394-307">Par exemple, la modification de la propriété <a href="extendedproperty-propid.md"><strong>propid</strong></a> d’un objet <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> n’est pas autorisée si l’objet est attaché à un certificat.</span><span class="sxs-lookup"><span data-stu-id="97394-307">For example, changing the <a href="extendedproperty-propid.md"><strong>PropID</strong></a> property of an <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> object is not allowed if the object is attached to a certificate.</span></span><br/></td>
<td><span data-ttu-id="97394-308">0x80880903//v 2.0</span><span class="sxs-lookup"><span data-stu-id="97394-308">0x80880903 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97394-309"><strong>CAPICOM_E_OUT_OF_RESOURCE</strong></span><span class="sxs-lookup"><span data-stu-id="97394-309"><strong>CAPICOM_E_OUT_OF_RESOURCE</strong></span></span></td>
<td><span data-ttu-id="97394-310">CAPICOM n’a plus de ressources.</span><span class="sxs-lookup"><span data-stu-id="97394-310">CAPICOM has run out of a resource.</span></span><br/></td>
<td><span data-ttu-id="97394-311">0x80880904//v 2.0</span><span class="sxs-lookup"><span data-stu-id="97394-311">0x80880904 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97394-312"><strong>CAPICOM_E_INTERNAL</strong></span><span class="sxs-lookup"><span data-stu-id="97394-312"><strong>CAPICOM_E_INTERNAL</strong></span></span></td>
<td><span data-ttu-id="97394-313">Une erreur interne s'est produite.</span><span class="sxs-lookup"><span data-stu-id="97394-313">An internal error has occurred.</span></span> <br/> <span data-ttu-id="97394-314">Contactez le support technique Microsoft pour obtenir de l’aide.</span><span class="sxs-lookup"><span data-stu-id="97394-314">Contact Microsoft Technical Support for assistance.</span></span><br/></td>
<td><span data-ttu-id="97394-315">0x80880911</span><span class="sxs-lookup"><span data-stu-id="97394-315">0x80880911</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97394-316"><strong>CAPICOM_E_UNKNOWN</strong></span><span class="sxs-lookup"><span data-stu-id="97394-316"><strong>CAPICOM_E_UNKNOWN</strong></span></span></td>
<td><span data-ttu-id="97394-317">Une erreur inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="97394-317">An unknown error has occurred.</span></span> <br/> <span data-ttu-id="97394-318">Collectez autant d’informations que possible et contactez votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="97394-318">Collect as much information as possible, and contact your vendor.</span></span><br/></td>
<td><span data-ttu-id="97394-319">0x80880999</span><span class="sxs-lookup"><span data-stu-id="97394-319">0x80880999</span></span></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="97394-320">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97394-320">Requirements</span></span>



| <span data-ttu-id="97394-321">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97394-321">Requirement</span></span> | <span data-ttu-id="97394-322">Valeur</span><span class="sxs-lookup"><span data-stu-id="97394-322">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="97394-323">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="97394-323">Redistributable</span></span><br/> | <span data-ttu-id="97394-324">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="97394-324">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="97394-325">En-tête</span><span class="sxs-lookup"><span data-stu-id="97394-325">Header</span></span><br/>          | <dl> <span data-ttu-id="97394-326"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="97394-326"><dt>Capicom.h</dt></span></span> </dl> |



 

 




