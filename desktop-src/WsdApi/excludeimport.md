---
description: 'Empêche la génération d’instructions d’importation pour des cibles spécifiées nommées dans un élément wsdl : import dans un fichier WSDL.'
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: élément excludeImport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e14d79576151fbb3dc266621c3fa34816cea55e5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995876"
---
# <a name="excludeimport-element"></a>élément excludeImport

Empêche la génération d’instructions d’importation pour des cibles spécifiées nommées dans un \<wsdl:import> élément d’un fichier WSDL. Cela peut être utilisé pour empêcher WsdCodeGen d’importer des cibles connues, telles que les spécifications WS-Addressing et WS-Eventing, même si ces cibles sont référencées dans le WSDL.

La valeur de cet élément doit être définie sur l’espace de noms nommé dans l' \<wsdl:import> élément à exclure.

## <a name="usage"></a>Usage

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



| Étiquette | Value |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




