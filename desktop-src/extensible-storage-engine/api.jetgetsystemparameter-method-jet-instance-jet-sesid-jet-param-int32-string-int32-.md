---
description: 'En savoir plus sur : méthode API. JetGetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)'
title: Méthode API. JetGetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)
TOCTitle: JetGetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetSystemParameter(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_param,System.Int32@,System.String@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetsystemparameter(v=EXCHG.10)
ms:contentKeyID: 55100727
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetSystemParameter
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 840c17ef1d74b57b4bee75b9efafe5a314f09a57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862229"
---
# <a name="apijetgetsystemparameter-method-jet_instance-jet_sesid-jet_param-int32-string-int32"></a><span data-ttu-id="7966a-103">Méthode API. JetGetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)</span><span class="sxs-lookup"><span data-stu-id="7966a-103">Api.JetGetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)</span></span>

<span data-ttu-id="7966a-104">Obtient les options de configuration de base de données.</span><span class="sxs-lookup"><span data-stu-id="7966a-104">Gets database configuration options.</span></span>

<span data-ttu-id="7966a-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7966a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7966a-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7966a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7966a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7966a-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetGetSystemParameter ( _
    instance As JET_INSTANCE, _
    sesid As JET_SESID, _
    paramid As JET_param, _
    ByRef paramValue As Integer, _
    <OutAttribute> ByRef paramString As String, _
    maxParam As Integer _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim paramid As JET_param
Dim paramValue As Integer
Dim paramString As String
Dim maxParam As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetGetSystemParameter(instance, _
    sesid, paramid, paramValue, paramString, _
    maxParam)
```

``` csharp
public static JET_wrn JetGetSystemParameter(
    JET_INSTANCE instance,
    JET_SESID sesid,
    JET_param paramid,
    ref int paramValue,
    out string paramString,
    int maxParam
)
```

#### <a name="parameters"></a><span data-ttu-id="7966a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7966a-108">Parameters</span></span>

  - <span data-ttu-id="7966a-109">instance</span><span class="sxs-lookup"><span data-stu-id="7966a-109">instance</span></span>  
    <span data-ttu-id="7966a-110">Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7966a-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="7966a-111">Instance de à partir de laquelle récupérer les options.</span><span class="sxs-lookup"><span data-stu-id="7966a-111">The instance to retrieve the options from.</span></span>

<!-- end list -->

  - <span data-ttu-id="7966a-112">sesid</span><span class="sxs-lookup"><span data-stu-id="7966a-112">sesid</span></span>  
    <span data-ttu-id="7966a-113">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7966a-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7966a-114">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="7966a-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="7966a-115">paramid</span><span class="sxs-lookup"><span data-stu-id="7966a-115">paramid</span></span>  
    <span data-ttu-id="7966a-116">Type : [Microsoft.ISAM.esent.Interop.JET_param](./jet-param-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7966a-116">Type: [Microsoft.Isam.Esent.Interop.JET_param](./jet-param-enumeration.md)</span></span>  
    
    <span data-ttu-id="7966a-117">Paramètre à récupérer.</span><span class="sxs-lookup"><span data-stu-id="7966a-117">The parameter to get.</span></span>

<!-- end list -->

  - <span data-ttu-id="7966a-118">Valeur paramValue</span><span class="sxs-lookup"><span data-stu-id="7966a-118">paramValue</span></span>  
    <span data-ttu-id="7966a-119">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7966a-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="7966a-120">Retourne la valeur du paramètre, si la valeur est un entier.</span><span class="sxs-lookup"><span data-stu-id="7966a-120">Returns the value of the parameter, if the value is an integer.</span></span>

<!-- end list -->

  - <span data-ttu-id="7966a-121">paramString</span><span class="sxs-lookup"><span data-stu-id="7966a-121">paramString</span></span>  
    <span data-ttu-id="7966a-122">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="7966a-122">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="7966a-123">Retourne la valeur du paramètre, si la valeur est une chaîne.</span><span class="sxs-lookup"><span data-stu-id="7966a-123">Returns the value of the parameter, if the value is a string.</span></span>

<!-- end list -->

  - <span data-ttu-id="7966a-124">maxParam</span><span class="sxs-lookup"><span data-stu-id="7966a-124">maxParam</span></span>  
    <span data-ttu-id="7966a-125">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7966a-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="7966a-126">Taille maximale de la chaîne de paramètre.</span><span class="sxs-lookup"><span data-stu-id="7966a-126">The maximum size of the parameter string.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7966a-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7966a-127">Return value</span></span>

<span data-ttu-id="7966a-128">Type : [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7966a-128">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="7966a-129">Code d’avertissement ESENT.</span><span class="sxs-lookup"><span data-stu-id="7966a-129">An ESENT warning code.</span></span>  

## <a name="remarks"></a><span data-ttu-id="7966a-130">Notes</span><span class="sxs-lookup"><span data-stu-id="7966a-130">Remarks</span></span>

<span data-ttu-id="7966a-131">[ErrorToString](./jet-param-enumeration.md) passe le numéro d’erreur dans valeur paramValue, ce qui explique pourquoi il s’agit d’un paramètre ref et non d’un paramètre out.</span><span class="sxs-lookup"><span data-stu-id="7966a-131">[ErrorToString](./jet-param-enumeration.md) passes in the error number in the paramValue, which is why it is a ref parameter and not an out parameter.</span></span>

## <a name="see-also"></a><span data-ttu-id="7966a-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7966a-132">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7966a-133">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="7966a-133">Reference</span></span>

[<span data-ttu-id="7966a-134">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="7966a-134">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7966a-135">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="7966a-135">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7966a-136">Surcharge JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="7966a-136">JetGetSystemParameter overload</span></span>](./api.jetgetsystemparameter-method.md)

[<span data-ttu-id="7966a-137">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7966a-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
