---
title: Type complexe TLSExtensionsType
description: En savoir plus sur le type complexe TLSExtensionsType. Ce type active les améliorations futures du schéma.
ms.assetid: 5e4f8ef8-1adb-4683-8001-ba7d2d392523
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833a93b9ecb0ba32a95e4c85856ac015f5135fb5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730332"
---
# <a name="tlsextensionstype-complex-type"></a><span data-ttu-id="b60b0-104">Type complexe TLSExtensionsType</span><span class="sxs-lookup"><span data-stu-id="b60b0-104">TLSExtensionsType Complex Type</span></span>

<span data-ttu-id="b60b0-105">Le type complexe **TLSExtensionsType** permet de futures améliorations du schéma.</span><span class="sxs-lookup"><span data-stu-id="b60b0-105">The **TLSExtensionsType** complex type enables future enhancements to the schema.</span></span>


```XML
<xs:complexType name="TLSExtensionsType">
    <xs:sequence>
        <xs:any processContents="lax" 
            minOccurs="0" 
            maxOccurs="unbounded" 
            namespace="##other"
        />
    <xs:sequence>
</xs:complexType>

```



## <a name="remarks"></a><span data-ttu-id="b60b0-106">Notes</span><span class="sxs-lookup"><span data-stu-id="b60b0-106">Remarks</span></span>

<span data-ttu-id="b60b0-107">L’élément **TLSExtensionsType** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="b60b0-107">The **TLSExtensionsType** element is optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b60b0-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b60b0-108">Related topics</span></span>

<dl> <span data-ttu-id="b60b0-109"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="b60b0-109"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="b60b0-110">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="b60b0-110">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="b60b0-111">eaptlsconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="b60b0-111">eaptlsconnectionpropertiesv2</span></span>](eaptlsconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="b60b0-112">Types complexes eaptlsconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="b60b0-112">eaptlsconnectionpropertiesv2 Complex Types</span></span>](eaptlsconnectionpropertiesv2schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="b60b0-113">**TLSExtensions (TLSExtensionsType)**</span><span class="sxs-lookup"><span data-stu-id="b60b0-113">**TLSExtensions (TLSExtensionsType)**</span></span>](eaptlsconnectionpropertiesv2schema-performservervalidation-eaptype-element.md)
</dt> </dl>

 

 




