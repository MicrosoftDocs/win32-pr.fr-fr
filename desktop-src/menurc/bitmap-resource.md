---
title: Ressource BITMAP
description: Définit une image bitmap qu’une application utilise dans son affichage d’écran ou en tant qu’élément dans un menu ou un contrôle.
ms.assetid: 2db2f7f0-735f-4aac-9813-c04a2f7788b2
keywords:
- Menus des ressources BITMAP et autres ressources
topic_type:
- apiref
api_name:
- BITMAP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff75f235e8aa1787e93f9420b4d7ed27f440cdc09510547295ebced4ec494bdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118734897"
---
# <a name="bitmap-resource"></a>Ressource BITMAP

Définit une image bitmap qu’une application utilise dans son affichage d’écran ou en tant qu’élément dans un menu ou un contrôle.

``` syntax
nameID BITMAP filename
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nom unique ou valeur d’entier non signé 16 bits identifiant la ressource.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*extension*
</dt> <dd>

Nom du fichier qui contient la ressource. Le nom doit être un nom de fichier valide ; il doit s’agir d’un chemin d’accès complet si le fichier ne se trouve pas dans le répertoire de travail actuel. Le chemin d’accès doit être une chaîne entre guillemets.

</dd> </dl>

Certains attributs sont également pris en charge pour la compatibilité descendante. Pour plus d’informations, consultez [attributs de ressource communs](common-resource-attributes.md).

## <a name="examples"></a>Exemples

L’exemple suivant définit deux ressources bitmap :

``` syntax
disk1   BITMAP "disk.bmp"
12      BITMAP "diskette.bmp"
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation des bitmaps](/windows/desktop/gdi/using-bitmaps)
</dt> <dt>

[**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa)
</dt> <dt>

[**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea)
</dt> </dl>

 

 