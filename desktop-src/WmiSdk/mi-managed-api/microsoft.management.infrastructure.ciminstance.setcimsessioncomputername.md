---
description: 'En savoir plus sur : méthode CimInstance. SetCimSessionComputerName (String)'
title: CimInstance.SetCimSessionComputerName, méthode (Microsoft.Management.Infrastructure)
TOCTitle: CimInstance.SetCimSessionComputerName method (Microsoft.Management.Infrastructure)
ms:assetid: M:Microsoft.Management.Infrastructure.CimInstance.SetCimSessionComputerName(System.String)
ms.date: 11/12/2019
mtps_version: v=VS.85
f1_keywords:
- Microsoft.Management.Infrastructure.CimInstance.SetCimSessionComputerName
- Microsoft::Management::Infrastructure::CimInstance::SetCimSessionComputerName
dev_langs:
- CSharp
- C++
- VB
- FSharp
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.CimInstance.SetCimSessionComputerName
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: b9f4cd9d308617a2369eaa542705e4ad7f854fa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319574"
---
# <a name="ciminstancesetcimsessioncomputername-method-string"></a>Méthode CimInstance. SetCimSessionComputerName (String)

Définit le nom de l’ordinateur utilisé pour la session CIM.

**Espace de noms :**   [Microsoft. Management. infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958\(v=vs.85\))  
**Assembly :**  Microsoft. Management. infrastructure (en Microsoft.Management.Infrastructure.dll)  

## <a name="syntax"></a>Syntaxe

``` csharp
public void SetCimSessionComputerName(
    string computerName
)
```

``` c++
public:
void SetCimSessionComputerName(
    String^ computerName
)
```

``` fsharp
member SetCimSessionComputerName : 
        computerName:string -> unit
```

``` vb
Public Sub SetCimSessionComputerName (
    computerName As String
)
```

#### <a name="parameters"></a>Paramètres

  - computerName  
    Type : [System. String](/dotnet/api/system.string?view=netframework-4.8)
    
    Nom de l’ordinateur utilisé pour la session CIM. **null** si l’instance actuelle est uniquement côté client ou si l’instance a été récupérée à partir de localhost.

## <a name="see-also"></a>Voir aussi

[CimInstance, classe](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336\(v=vs.85\))  
[Espace de noms Microsoft. Management. infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958\(v=vs.85\))
