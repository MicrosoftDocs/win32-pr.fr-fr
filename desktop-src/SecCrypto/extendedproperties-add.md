---
description: Ajoute une propriété étendue à la collection.
ms.assetid: 1d6b3c39-17b0-4a7c-a5c2-4a3bd866be07
title: ExtendedProperties. Add, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 06e4170b34dcdca97bc0bae6bb48b4a057a8e9b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543241"
---
# <a name="extendedpropertiesadd-method"></a><span data-ttu-id="68240-103">ExtendedProperties. Add, méthode</span><span class="sxs-lookup"><span data-stu-id="68240-103">ExtendedProperties.Add method</span></span>

<span data-ttu-id="68240-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="68240-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="68240-105">Utilisez plutôt les services d’appel de plateforme (PInvoke) pour appeler la fonction API Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) et obtenir les propriétés.</span><span class="sxs-lookup"><span data-stu-id="68240-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="68240-106">Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="68240-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="68240-107">Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]</span><span class="sxs-lookup"><span data-stu-id="68240-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="68240-108">La méthode **Add** ajoute une propriété étendue à la collection.</span><span class="sxs-lookup"><span data-stu-id="68240-108">The **Add** method adds an extended property to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="68240-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68240-109">Syntax</span></span>


```VB
ExtendedProperties.Add( _
  ByVal valProperty _
)
```



## <a name="parameters"></a><span data-ttu-id="68240-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68240-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68240-111">*valProperty* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="68240-111">*valProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68240-112">Objet [**ExtendedProperty**](extendedproperty.md) qui représente la propriété étendue.</span><span class="sxs-lookup"><span data-stu-id="68240-112">An [**ExtendedProperty**](extendedproperty.md) object that represents the extended property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68240-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="68240-113">Return value</span></span>

<span data-ttu-id="68240-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="68240-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="68240-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68240-115">Requirements</span></span>



| <span data-ttu-id="68240-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68240-116">Requirement</span></span> | <span data-ttu-id="68240-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="68240-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68240-118">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="68240-118">End of client support</span></span><br/> | <span data-ttu-id="68240-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68240-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="68240-120">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="68240-120">End of server support</span></span><br/> | <span data-ttu-id="68240-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68240-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="68240-122">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="68240-122">Redistributable</span></span><br/>       | <span data-ttu-id="68240-123">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="68240-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="68240-124">DLL</span><span class="sxs-lookup"><span data-stu-id="68240-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="68240-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68240-125"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
