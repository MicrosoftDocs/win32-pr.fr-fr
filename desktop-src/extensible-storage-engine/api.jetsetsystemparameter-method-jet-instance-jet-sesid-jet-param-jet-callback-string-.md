---
description: 'En savoir plus sur : méthode API. JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, String)'
title: Méthode API. JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, String)
TOCTitle: JetSetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_param,Microsoft.Isam.Esent.Interop.JET_CALLBACK,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetsystemparameter(v=EXCHG.10)
ms:contentKeyID: 55100819
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2d8d9d65af803a011c0a6a79fdaec2fb0a44755b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104211058"
---
# <a name="apijetsetsystemparameter-method-jet_instance-jet_sesid-jet_param-jet_callback-string"></a><span data-ttu-id="3cafc-103">Méthode API. JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, String)</span><span class="sxs-lookup"><span data-stu-id="3cafc-103">Api.JetSetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, String)</span></span>

<span data-ttu-id="3cafc-104">Définit les options de configuration de la base de données.</span><span class="sxs-lookup"><span data-stu-id="3cafc-104">Sets database configuration options.</span></span>

<span data-ttu-id="3cafc-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3cafc-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3cafc-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3cafc-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3cafc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3cafc-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetSetSystemParameter ( _
    instance As JET_INSTANCE, _
    sesid As JET_SESID, _
    paramid As JET_param, _
    paramValue As JET_CALLBACK, _
    paramString As String _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim paramid As JET_param
Dim paramValue As JET_CALLBACK
Dim paramString As String
Dim returnValue As JET_wrn

returnValue = Api.JetSetSystemParameter(instance, _
    sesid, paramid, paramValue, paramString)
```

``` csharp
public static JET_wrn JetSetSystemParameter(
    JET_INSTANCE instance,
    JET_SESID sesid,
    JET_param paramid,
    JET_CALLBACK paramValue,
    string paramString
)
```

#### <a name="parameters"></a><span data-ttu-id="3cafc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3cafc-108">Parameters</span></span>

  - <span data-ttu-id="3cafc-109">instance</span><span class="sxs-lookup"><span data-stu-id="3cafc-109">instance</span></span>  
    <span data-ttu-id="3cafc-110">Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3cafc-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="3cafc-111">Instance sur laquelle définir l’option ou [Nil](./jet-instance.nil-property.md) pour définir l’option sur toutes les instances.</span><span class="sxs-lookup"><span data-stu-id="3cafc-111">The instance to set the option on or [Nil](./jet-instance.nil-property.md) to set the option on all instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="3cafc-112">sesid</span><span class="sxs-lookup"><span data-stu-id="3cafc-112">sesid</span></span>  
    <span data-ttu-id="3cafc-113">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3cafc-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="3cafc-114">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="3cafc-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="3cafc-115">paramid</span><span class="sxs-lookup"><span data-stu-id="3cafc-115">paramid</span></span>  
    <span data-ttu-id="3cafc-116">Type : [Microsoft.ISAM.esent.Interop.JET_param](./jet-param-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="3cafc-116">Type: [Microsoft.Isam.Esent.Interop.JET_param](./jet-param-enumeration.md)</span></span>  
    
    <span data-ttu-id="3cafc-117">Paramètre à définir.</span><span class="sxs-lookup"><span data-stu-id="3cafc-117">The parameter to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="3cafc-118">Valeur paramValue</span><span class="sxs-lookup"><span data-stu-id="3cafc-118">paramValue</span></span>  
    <span data-ttu-id="3cafc-119">Type : [Microsoft.ISAM.esent.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="3cafc-119">Type: [Microsoft.Isam.Esent.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span></span>  
    
    <span data-ttu-id="3cafc-120">Valeur du paramètre à définir, si le paramètre est un JET_CALLBACK.</span><span class="sxs-lookup"><span data-stu-id="3cafc-120">The value of the parameter to set, if the parameter is a JET_CALLBACK.</span></span>

<!-- end list -->

  - <span data-ttu-id="3cafc-121">paramString</span><span class="sxs-lookup"><span data-stu-id="3cafc-121">paramString</span></span>  
    <span data-ttu-id="3cafc-122">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="3cafc-122">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="3cafc-123">Valeur du paramètre à définir, si le paramètre est un type chaîne.</span><span class="sxs-lookup"><span data-stu-id="3cafc-123">The value of the parameter to set, if the parameter is a string type.</span></span>

#### <a name="return-value"></a><span data-ttu-id="3cafc-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3cafc-124">Return value</span></span>

<span data-ttu-id="3cafc-125">Type : [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="3cafc-125">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="3cafc-126">Code d’avertissement ESENT.</span><span class="sxs-lookup"><span data-stu-id="3cafc-126">An ESENT warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3cafc-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3cafc-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3cafc-128">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="3cafc-128">Reference</span></span>

[<span data-ttu-id="3cafc-129">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="3cafc-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3cafc-130">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="3cafc-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3cafc-131">Surcharge JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="3cafc-131">JetSetSystemParameter overload</span></span>](./api.jetsetsystemparameter-method.md)

[<span data-ttu-id="3cafc-132">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3cafc-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
