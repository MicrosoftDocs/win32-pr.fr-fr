---
description: La table CCPSearch contient la liste des signatures de fichiers utilisées pour le programme de vérification de la compatibilité (CCP). Au moins l’un de ces fichiers doit être présent sur l’ordinateur d’un utilisateur pour que l’utilisateur soit compatible avec le programme.
ms.assetid: 98d21e24-1633-44b7-bfdb-5a40bab8d319
title: Table CCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368c0452fea011aca1080ca17020467ba6e0dc4f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092294"
---
# <a name="ccpsearch-table"></a>Table CCPSearch

La table CCPSearch contient la liste des signatures de fichiers utilisées pour le programme de vérification de la compatibilité (CCP). Au moins l’un de ces fichiers doit être présent sur l’ordinateur d’un utilisateur pour que l’utilisateur soit compatible avec le programme.

La table CCPSearch contient la colonne suivante.



| Colonne      | Type                         | Clé | Nullable |
|-------------|------------------------------|-----|----------|
| Signature\_ | [Identificateur](identifier.md) | O   | N        |



 

## <a name="column"></a>Colonne

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_
</dt> <dd>

La signature \_ représente une signature de fichier unique et est également la clé externe dans les tables [signature](signature-table.md), [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md)et [DrLocator](drlocator-table.md) .

</dd> </dl>

## <a name="remarks"></a>Notes

Cette table est référencée lorsque l' [action CCPSearch](ccpsearch-action.md) ou l' [action RMCCPSearch](rmccpsearch-action.md) est exécutée.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



