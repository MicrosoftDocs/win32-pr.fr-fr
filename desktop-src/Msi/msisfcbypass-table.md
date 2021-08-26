---
description: la Table MsiSFCBypass contient une liste de fichiers qui doivent contourner Windows Protection des fichiers lorsque les fichiers sont installés sur Microsoft Windows Me.
ms.assetid: 86de0dc1-ed8f-410c-a411-6c44c8e5c9fd
title: Table MsiSFCBypass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d233f09aa62b5f6d17112b1f5a98753e328f3a1746c452de5a5a1689a36f971f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042669"
---
# <a name="msisfcbypass-table"></a>Table MsiSFCBypass

la Table MsiSFCBypass contient une liste de fichiers qui doivent contourner Windows Protection des fichiers lorsque les fichiers sont installés sur Microsoft Windows Me.

La table MsiSFCBypass contient la colonne suivante.



| Colonne | Type                         | Clé | Nullable |
|--------|------------------------------|-----|----------|
| fichier\_ | [Identificateur](identifier.md) | O   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Txt\_
</dt> <dd>

clé étrangère de la [Table de fichiers](file-table.md) qui spécifie le fichier qui doit contourner Windows Protection de fichier lorsque le fichier est installé sur Windows Me.

</dd> </dl>

 

 



