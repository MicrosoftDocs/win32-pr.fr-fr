---
description: Génère des constantes C pour les types de ports.
ms.assetid: 6ad0d163-df51-48b6-aad7-a4b018688872
title: élément portTypeDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60f55408df938ed95af14c69b2676473ac1bda71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203001"
---
# <a name="porttypedefinitions-element"></a>élément portTypeDefinitions

Génère des constantes C pour les types de ports.

## <a name="usage"></a>Utilisation

``` syntax
<portTypeDefinitions>
  child elements
</portTypeDefinitions>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                                   | Description                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Baptisé**](codename.md)<br/>                   | Spécifie le nom à utiliser pour le type de port dans le code généré. Par défaut, le nom de code est généré à partir du nom qualifié du type de port.<br/> <br/>         |
| [**eventStubFunction**](eventstubfunction.md)<br/> | Spécifie si les références de fonction stub doivent être incluses dans les structures d’opération dans les définitions de type de port pour les opérations de notification.<br/> <br/>        |
| [**opération**](operation.md)<br/>                 | Spécifie une opération pour laquelle du code doit être généré.<br/> <br/>                                                                                                  |
| [**portType**](porttype.md)<br/>                   | Spécifie le type de port pour lequel le code doit être généré.<br/> <br/>                                                                                                 |
| [**stubFunction**](stubfunction.md)<br/>           | Spécifie si les références de fonction stub doivent être incluses dans les structures d’opération dans les définitions de type de port pour les opérations unidirectionnelles et bidirectionnelles.<br/> <br/> |



### <a name="child-element-sequence"></a>Séquence d’éléments enfants

``` syntax
(
  portType?, 
  operation*, 
  stubFunction?, 
  eventStubFunction?, 
  codeName?
)
```

## <a name="parent-elements"></a>Éléments parents



| Élément                         | Description                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**fichier**](file.md)<br/> | Génère un fichier à partir du générateur de code.<br/> <br/> |



## <a name="remarks"></a>Notes

Cet élément est généralement utilisé dans les fichiers sources C pour fournir les constantes de type de port déclarées par [**portTypeDeclarations**](porttypedeclarations.md).

## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




