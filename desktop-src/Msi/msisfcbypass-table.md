---
description: La table MsiSFCBypass contient une liste de fichiers qui doivent contourner la protection des fichiers Windows lorsque les fichiers sont installés sur Microsoft Windows Me.
ms.assetid: 86de0dc1-ed8f-410c-a411-6c44c8e5c9fd
title: Table MsiSFCBypass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 707294e9461aaf321add8a3959682a0db555cc2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319910"
---
# <a name="msisfcbypass-table"></a>Table MsiSFCBypass

La table MsiSFCBypass contient une liste de fichiers qui doivent contourner la protection des fichiers Windows lorsque les fichiers sont installés sur Microsoft Windows Me.

La table MsiSFCBypass contient la colonne suivante.



| Colonne | Type                         | Clé | Nullable |
|--------|------------------------------|-----|----------|
| fichier\_ | [Identificateur](identifier.md) | O   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Txt\_
</dt> <dd>

Clé étrangère de la [table de fichiers](file-table.md) qui spécifie le fichier qui doit contourner la protection des fichiers Windows lorsque le fichier est installé sur Windows Me.

</dd> </dl>

 

 



