---
description: La propriété Item récupère un objet ExtendedProperty à partir de la collection. Il s’agit de la propriété par défaut.
ms.assetid: add819e1-6330-483a-8a76-3b7fb8d3f110
title: ExtendedProperties. Item, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 200e36f232c97c1b5a86c8a8a975783469d64a71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526521"
---
# <a name="extendedpropertiesitem-property"></a><span data-ttu-id="f05fa-104">ExtendedProperties. Item, propriété</span><span class="sxs-lookup"><span data-stu-id="f05fa-104">ExtendedProperties.Item property</span></span>

<span data-ttu-id="f05fa-105">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f05fa-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f05fa-106">Utilisez plutôt les services d’appel de plateforme (PInvoke) pour appeler la fonction API Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) et obtenir les propriétés.</span><span class="sxs-lookup"><span data-stu-id="f05fa-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="f05fa-107">Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="f05fa-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="f05fa-108">Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]</span><span class="sxs-lookup"><span data-stu-id="f05fa-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="f05fa-109">La propriété **Item** récupère un objet [**ExtendedProperty**](extendedproperty.md) à partir de la collection.</span><span class="sxs-lookup"><span data-stu-id="f05fa-109">The **Item** property retrieves an [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span> <span data-ttu-id="f05fa-110">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="f05fa-110">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="f05fa-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f05fa-111">Syntax</span></span>


```VB
ExtendedProperties.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="f05fa-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f05fa-112">Property value</span></span>

<span data-ttu-id="f05fa-113">Objet [**ExtendedProperty**](extendedproperty.md) qui représente la propriété étendue indexée de la collection.</span><span class="sxs-lookup"><span data-stu-id="f05fa-113">An [**ExtendedProperty**](extendedproperty.md) object that represents the indexed extended property of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="f05fa-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f05fa-114">Requirements</span></span>



| <span data-ttu-id="f05fa-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f05fa-115">Requirement</span></span> | <span data-ttu-id="f05fa-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f05fa-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f05fa-117">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f05fa-117">End of client support</span></span><br/> | <span data-ttu-id="f05fa-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f05fa-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f05fa-119">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="f05fa-119">End of server support</span></span><br/> | <span data-ttu-id="f05fa-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f05fa-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f05fa-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="f05fa-121">Redistributable</span></span><br/>       | <span data-ttu-id="f05fa-122">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="f05fa-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f05fa-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f05fa-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f05fa-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f05fa-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
