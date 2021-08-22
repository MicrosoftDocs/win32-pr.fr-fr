---
title: Prise en charge d’ID3
description: ID3 est une organisation qui a défini un ensemble de normes pour inclure les métadonnées dans les fichiers audio MPEG Layer-3 (MP3).
ms.assetid: 8c1f1114-48d8-4dce-b7ab-0293265a875c
keywords:
- Windows Media Format SDK, prise en charge d’ID3
- ASF (Advanced Systems Format), prise en charge d’ID3
- ASF (format des systèmes avancés), prise en charge d’ID3
- métadonnées, ID3
- ID3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27c92fb9282483b6fd01b1149220e5f30421c3c1285bd533d64afef91709314e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118702980"
---
# <a name="id3-support"></a>Prise en charge d’ID3

ID3 est une organisation qui a défini un ensemble de normes pour inclure les métadonnées dans les fichiers audio MPEG Layer-3 (MP3). les objets du kit de développement logiciel (SDK) Windows Media Format fournissent la prise en charge des attributs compatibles ID3. Trois versions de ID3 distinctes sont prises en charge : ID3v1. x, ID3v 2.2 et ID3v 2.3/v2, 4. Pour obtenir la liste des attributs qui correspondent aux frames ID3, consultez [prise en charge des balises ID3](id3-tag-support.md).

Sauf indication contraire, aucune validation des données de trame ID3 n’est effectuée par les objets de ce kit de développement logiciel (SDK). Par exemple, l’attribut de métadonnées [**WM/paroles \_ synchronisées**](wm-lyrics-synchronised.md) stocke les paroles des chansons avec les horodatages correspondants. Lors de l’écriture d’un attribut **\_ synchronisé WM/paroles** , les objets de ce kit de développement logiciel (SDK) ne vérifient pas si les horodatages sont dans l’ordre chronologique ou s’ils effectuent la validation de tout type.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Attributs**](attributes.md)
</dt> <dt>

[**Fonctionnalités de métadonnées**](metadata-features.md)
</dt> <dt>

[**Utilisation des métadonnées**](working-with-metadata.md)
</dt> </dl>

 

 




