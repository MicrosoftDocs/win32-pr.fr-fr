---
description: 'En savoir plus sur : propriété InstanceParameters. EventSource'
title: InstanceParameters. EventSource, propriété
TOCTitle: 'EventSource property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.EventSource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.eventsource(v=EXCHG.10)
ms:contentKeyID: 55103563
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.EventSource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_EventSource
- Microsoft.Isam.Esent.Interop.InstanceParameters.EventSource
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_EventSource
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5cba0c6f9aef4b9e6633a5d0073b1fdbc2c3b1a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520700"
---
# <a name="instanceparameterseventsource-property"></a><span data-ttu-id="a583d-103">InstanceParameters. EventSource, propriété</span><span class="sxs-lookup"><span data-stu-id="a583d-103">InstanceParameters.EventSource property</span></span>

<span data-ttu-id="a583d-104">Obtient ou définit une chaîne spécifique à l’application qui sera ajoutée à tous les messages du journal des événements émis par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="a583d-104">Gets or sets an application specific string that will be added to any event log messages that are emitted by the database engine.</span></span> <span data-ttu-id="a583d-105">Cela permet de corréler facilement les messages du journal des événements avec l’application source.</span><span class="sxs-lookup"><span data-stu-id="a583d-105">This allows easy correlation of event log messages with the source application.</span></span> <span data-ttu-id="a583d-106">Par défaut, le nom de l’exécutable de l’application hôte sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="a583d-106">By default the host application executable name will be used.</span></span>

<span data-ttu-id="a583d-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a583d-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a583d-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a583d-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a583d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a583d-109">Syntax</span></span>

``` vb
'Declaration
Public Property EventSource As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.EventSource

instance.EventSource = value
```

``` csharp
public string EventSource { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="a583d-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a583d-110">Property value</span></span>

<span data-ttu-id="a583d-111">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="a583d-111">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="see-also"></a><span data-ttu-id="a583d-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a583d-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a583d-113">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="a583d-113">Reference</span></span>

[<span data-ttu-id="a583d-114">InstanceParameters, classe</span><span class="sxs-lookup"><span data-stu-id="a583d-114">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="a583d-115">Membres InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="a583d-115">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="a583d-116">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a583d-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
