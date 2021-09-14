---
description: La table FileSFPCatalog associe les fichiers spécifiés aux fichiers de catalogue utilisés par la protection des fichiers système.
ms.assetid: 70c8b64a-cf15-411c-8388-4a7e3051f45c
title: Table FileSFPCatalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2300b73cc1639d8a54e206ea609043cf657c91f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021728"
---
# <a name="filesfpcatalog-table"></a>Table FileSFPCatalog

La table FileSFPCatalog associe les fichiers spécifiés aux fichiers de catalogue utilisés par la protection des fichiers système.

**Windows Vista, Windows Server 2003 et Windows XP :** Non pris en charge.

La table FileSFPCatalog contient les colonnes suivantes.



| Colonne       | Type                         | Clé | Nullable |
|--------------|------------------------------|-----|----------|
| fichier\_       | [Identificateur](identifier.md) | O   | N        |
| SFPCatalog\_ | [Nom du fichier](filename.md)     | O   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Txt\_
</dt> <dd>

Clé étrangère vers la [table de fichiers](file-table.md).

</dd> <dt>

<span id="SFPCatalog_"></span><span id="sfpcatalog_"></span><span id="SFPCATALOG_"></span>SFPCatalog\_
</dt> <dd>

Clé étrangère vers la [table SFPCatalog](sfpcatalog-table.md).

</dd> </dl>

## <a name="remarks"></a>Notes

L' [action InstallSFPCatalogFile](installsfpcatalogfile-action.md) interroge la table de [composants](component-table.md), la [table de fichiers](file-table.md), la table FileSFPCatalog et la [table SFPCatalog](sfpcatalog-table.md).

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE76](ice76.md)  
</dl>

 

 



