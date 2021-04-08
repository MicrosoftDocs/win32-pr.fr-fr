---
description: 'Empêche la génération d’instructions d’importation pour des cibles spécifiées nommées dans un <élément wsdl : import> dans un fichier WSDL.'
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: élément excludeImport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c08d8880029d9e03917e48b61561e3ab3eb2815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863998"
---
# <a name="excludeimport-element"></a>élément excludeImport

Empêche la génération d’instructions d’importation pour des cibles spécifiées nommées dans un <élément wsdl : import> dans un fichier WSDL. Cela peut être utilisé pour empêcher WsdCodeGen d’importer des cibles connues, telles que les spécifications WS-Addressing et WS-Eventing, même si ces cibles sont référencées dans le WSDL.

La valeur de cet élément doit être définie sur l’espace de noms nommé dans l’élément <wsdl : import> à exclure.

## <a name="usage"></a>Utilisation

``` syntax
<excludeImport/>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                         | Description                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [**WSDL**](wsdl.md)<br/> | Spécifie un fichier WSDL à traiter pour les informations de contrat.<br/> <br/> |



## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




