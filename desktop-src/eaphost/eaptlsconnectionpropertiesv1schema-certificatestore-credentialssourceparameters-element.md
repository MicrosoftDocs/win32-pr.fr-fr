---
title: Élément CertificateStore (CredentialsSourceParameters)
description: Indique que le protocole EAP-TLS doit lire le certificat du magasin My de l’utilisateur ou de l’ordinateur en cours d’authentification.
ms.assetid: 6b15c7cc-b686-4419-a962-e3dd6b4b84a6
keywords:
- Élément CertificateStore EAPHost
topic_type:
- apiref
api_name:
- CertificateStore
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc7c8841fe275d19752f8b774de5766b95824339
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508945"
---
# <a name="certificatestore-credentialssourceparameters-element"></a><span data-ttu-id="a378a-104">Élément CertificateStore (CredentialsSourceParameters)</span><span class="sxs-lookup"><span data-stu-id="a378a-104">CertificateStore (CredentialsSourceParameters) Element</span></span>

<span data-ttu-id="a378a-105">L’élément **CertificateStore (CredentialsSourceParameters)** indique que le protocole EAP-TLS doit lire le certificat du magasin My de l’utilisateur ou de l’ordinateur en cours d’authentification.</span><span class="sxs-lookup"><span data-stu-id="a378a-105">The **CertificateStore (CredentialsSourceParameters)** element indicates that EAP-TLS should read the certificate from the user's My Store, or the machine being authenticated.</span></span>

``` syntax
<xs:element name="CertificateStore"
    type="CertSelection"
 />
```

<span data-ttu-id="a378a-106">L’élément **CertificateStore** est défini par le type complexe [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a378a-106">The **CertificateStore** element is defined by the [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="a378a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="a378a-107">Remarks</span></span>

<span data-ttu-id="a378a-108">Les éléments **CertificateStore** et [**Smartcard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) ne peuvent pas être utilisés simultanément.</span><span class="sxs-lookup"><span data-stu-id="a378a-108">The **CertificateStore** and [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="a378a-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a378a-109">Requirements</span></span>



| <span data-ttu-id="a378a-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a378a-110">Requirement</span></span> | <span data-ttu-id="a378a-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="a378a-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a378a-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a378a-112">Minimum supported client</span></span><br/> | <span data-ttu-id="a378a-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a378a-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a378a-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a378a-114">Minimum supported server</span></span><br/> | <span data-ttu-id="a378a-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a378a-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a378a-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a378a-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="a378a-117">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="a378a-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a378a-118">**CredentialsSourceParameters**</span><span class="sxs-lookup"><span data-stu-id="a378a-118">**CredentialsSourceParameters**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="a378a-119">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="a378a-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a378a-120">**CredentialsSource (EapType)**</span><span class="sxs-lookup"><span data-stu-id="a378a-120">**CredentialsSource (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)
<span data-ttu-id="a378a-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="a378a-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="a378a-122">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="a378a-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="a378a-123">Schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="a378a-123">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="a378a-124">Éléments de schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="a378a-124">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





