---
title: Élément CredentialsBlob (EapHostUserCredentials)
description: Est utilisé lorsque la configuration de la méthode est un objet BLOB binaire au lieu du format texte XML.
ms.assetid: 9d03374b-74f6-428e-8d3e-f8dccf51884e
keywords:
- Élément CredentialsBlob EAPHost
topic_type:
- apiref
api_name:
- CredentialsBlob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1fe7514c3aff50a7ecddadb3d8073a37b6c770eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103237"
---
# <a name="credentialsblob-eaphostusercredentials-element"></a><span data-ttu-id="f6b86-104">Élément CredentialsBlob (EapHostUserCredentials)</span><span class="sxs-lookup"><span data-stu-id="f6b86-104">CredentialsBlob (EapHostUserCredentials) Element</span></span>

<span data-ttu-id="f6b86-105">L’élément **CredentialsBlob (EapHostUserCredentials)** est utilisé lorsque la configuration de la méthode est un objet blob binaire au lieu du format texte XML.</span><span class="sxs-lookup"><span data-stu-id="f6b86-105">The **CredentialsBlob (EapHostUserCredentials)** element is used when the method configuration is a binary BLOB instead of in XML text format.</span></span>

``` syntax
<xs:element name="CredentialsBlob"
    type="hexBinary"
 />
```

<span data-ttu-id="f6b86-106">L’élément **CredentialsBlob** est défini par l’élément [**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f6b86-106">The **CredentialsBlob** element is defined by the [**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6b86-107">Notes</span><span class="sxs-lookup"><span data-stu-id="f6b86-107">Remarks</span></span>

<span data-ttu-id="f6b86-108">Les [**informations d’identification**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) et les éléments **CredentialsBlob** ne peuvent pas être utilisés simultanément.</span><span class="sxs-lookup"><span data-stu-id="f6b86-108">The [**Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) and **CredentialsBlob** elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6b86-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f6b86-109">Requirements</span></span>



| <span data-ttu-id="f6b86-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f6b86-110">Requirement</span></span> | <span data-ttu-id="f6b86-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6b86-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f6b86-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6b86-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f6b86-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f6b86-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f6b86-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6b86-114">Minimum supported server</span></span><br/> | <span data-ttu-id="f6b86-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f6b86-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f6b86-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6b86-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="f6b86-117">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="f6b86-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f6b86-118">**EapHostUserCredentials**</span><span class="sxs-lookup"><span data-stu-id="f6b86-118">**EapHostUserCredentials**</span></span>](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

<span data-ttu-id="f6b86-119">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="f6b86-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f6b86-120">**EapHostUserCredentials**</span><span class="sxs-lookup"><span data-stu-id="f6b86-120">**EapHostUserCredentials**</span></span>](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

[<span data-ttu-id="f6b86-121">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="f6b86-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="f6b86-122">Schéma eaphostusercredentials</span><span class="sxs-lookup"><span data-stu-id="f6b86-122">eaphostusercredentials Schema</span></span>](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





