---
description: Récupère le nombre d’objets ExtendedProperty dans la collection.
ms.assetid: 50bc8485-7285-4704-80db-c2e0d68e8cb0
title: ExtendedProperties. Count (propriété)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d4370f7ce5fc215d18b0940d3dbc2edc221af536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532252"
---
# <a name="extendedpropertiescount-property"></a><span data-ttu-id="7a104-103">ExtendedProperties. Count (propriété)</span><span class="sxs-lookup"><span data-stu-id="7a104-103">ExtendedProperties.Count property</span></span>

<span data-ttu-id="7a104-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7a104-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="7a104-105">Utilisez plutôt les services d’appel de plateforme (PInvoke) pour appeler la fonction API Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) et obtenir les propriétés.</span><span class="sxs-lookup"><span data-stu-id="7a104-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="7a104-106">Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="7a104-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="7a104-107">Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]</span><span class="sxs-lookup"><span data-stu-id="7a104-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="7a104-108">La propriété **Count** récupère le nombre d’objets [**ExtendedProperty**](extendedproperty.md) dans la collection.</span><span class="sxs-lookup"><span data-stu-id="7a104-108">The **Count** property retrieves the number of [**ExtendedProperty**](extendedproperty.md) objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a104-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a104-109">Syntax</span></span>


```VB
ExtendedProperties.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="7a104-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7a104-110">Property value</span></span>

<span data-ttu-id="7a104-111">Nombre d’objets [**ExtendedProperty**](extendedproperty.md) dans la collection.</span><span class="sxs-lookup"><span data-stu-id="7a104-111">The number of [**ExtendedProperty**](extendedproperty.md) objects in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a104-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a104-112">Requirements</span></span>



| <span data-ttu-id="7a104-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a104-113">Requirement</span></span> | <span data-ttu-id="7a104-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a104-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a104-115">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="7a104-115">End of client support</span></span><br/> | <span data-ttu-id="7a104-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a104-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7a104-117">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="7a104-117">End of server support</span></span><br/> | <span data-ttu-id="7a104-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a104-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7a104-119">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="7a104-119">Redistributable</span></span><br/>       | <span data-ttu-id="7a104-120">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="7a104-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7a104-121">DLL</span><span class="sxs-lookup"><span data-stu-id="7a104-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7a104-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a104-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
