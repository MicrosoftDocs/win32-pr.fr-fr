---
description: La table AppSearch contient les propriétés nécessaires à la recherche d’un fichier ayant une signature de fichier particulière. La table AppSearch peut également être utilisée pour affecter à une propriété la valeur existante d’une entrée de registre ou .ini fichier.
ms.assetid: d560096f-6baa-4fea-8786-f4e3d5ee6bf4
title: Table AppSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 450ab07a397366ca01e664b88321942e4f6a7800cd9e04c4d0cbbe048eed8b87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045649"
---
# <a name="appsearch-table"></a>Table AppSearch

La table AppSearch contient les propriétés nécessaires à la recherche d’un fichier ayant une signature de fichier particulière. La table AppSearch peut également être utilisée pour affecter à une propriété la valeur existante d’une entrée de registre ou .ini fichier.

La table AppSearch contient les colonnes suivantes.



| Colonne      | Type                         | Clé | Nullable |
|-------------|------------------------------|-----|----------|
| Propriété    | [Identificateur](identifier.md) | O   | N        |
| Signature\_ | [Identificateur](identifier.md) | O   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriété
</dt> <dd>

L’exécution de l’action [AppSearch](appsearch-action.md) affecte à cette propriété l’emplacement du fichier indiqué par la \_ colonne signature. Cette propriété est définie si la signature de fichier existe sur l’ordinateur de l’utilisateur. Les propriétés utilisées dans cette colonne doivent être des propriétés [publiques](public-properties.md) et comporter un identificateur qui ne contient pas de minuscules.

La propriété figurant dans le champ de propriété peut être initialisée dans la table de [Propriétés](property-table.md) ou à partir d’une ligne de commande. Si l’action [AppSearch](appsearch-action.md) localise la signature, le programme d’installation remplace la valeur de propriété initialisée par la valeur trouvée. Si la signature est introuvable, la valeur initiale de la propriété est utilisée. Si la propriété n’a jamais été initialisée, la propriété est définie uniquement si la signature est trouvée. Dans le cas contraire, la propriété n’est pas définie.

</dd> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_
</dt> <dd>

La \_ colonne signature contient un identificateur unique appelé signature et est également une clé externe dans les tables [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md)et [DrLocator](drlocator-table.md) . Lors de la recherche d’un fichier, la valeur dans cette colonne doit également être une clé étrangère dans la table de [signatures](signature-table.md) . Si la valeur de cette colonne n’est pas indiquée dans la table de signatures, le programme d’installation détermine que la recherche concerne un répertoire.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’action [AppSearch](appsearch-action.md) dans les [*tables de séquence*](s-gly.md) traite les informations de cette table. Pour plus d’informations sur l’utilisation des *tables de séquences*, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).

L’action [AppSearch](appsearch-action.md) recherche les signatures à l’aide de la table [CompLocator](complocator-table.md) en premier, de la table [RegLocator](reglocator-table.md) , de la table [IniLocator](inilocator-table.md) , troisième, et enfin de la table [DrLocator](drlocator-table.md) . Les signatures de fichiers sont répertoriées dans la table de [signature](signature-table.md) . Une signature qui ne figure pas dans la table de signature désigne un répertoire et l’action définit la propriété sur le chemin d’accès au répertoire de cette signature.

Consultez [recherche d’applications, de fichiers, d’entrées de registre ou de .ini d’entrées de fichier existants](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE52](ice52.md)  
[ICE88](ice88.md)  
</dl>

 

 



