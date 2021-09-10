---
title: ToolBoxBitmap32
description: Identifie le nom de module et l’ID de ressource pour une image bitmap de 16 x 16 à utiliser pour la face d’un bouton de barre d’outils ou de boîte à outils.
ms.assetid: 87b3d8e1-4d54-465c-9e5e-5e4f7391f313
keywords:
- Clé de Registre ToolBoxBitmap32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2ca6208586e961c0b6f8fa666c5731bab38faa6
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363456"
---
# <a name="toolboxbitmap32"></a>ToolBoxBitmap32

Identifie le nom de module et l’ID de ressource pour une image bitmap de 16 x 16 à utiliser pour la face d’un bouton de barre d’outils ou de boîte à outils.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      ToolBoxBitmap32 = filename,  resourceID
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur de **reg \_ SZ** qui spécifie le nom du module et l’identificateur de ressource pour l’image bitmap.

la taille de l’icône de Windows standard est trop grande pour être utilisée à cet effet. Cela requiert des conteneurs de contrôle qui ont un mode création dans lequel l’un sélectionne des contrôles et les place sur un formulaire en cours de conception.

 

 




