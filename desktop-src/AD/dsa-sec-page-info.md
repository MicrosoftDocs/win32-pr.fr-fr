---
title: Structure DSA_SEC_PAGE_INFO
description: Utilisé avec la feuille de calcul WM \_ ADSPROP \_ et la \_ \_ feuille DSA, \_ créer des \_ \_ messages de notification pour définir une feuille de propriétés secondaire dans un composant logiciel enfichable MMC Active Directory.
ms.assetid: 422d84dc-6b5e-43bf-ac4f-3b99cb59f9df
ms.tgt_platform: multiple
keywords:
- DSA_SEC_PAGE_INFO structure Active Directory
- Pointeur de structure PDSA_SEC_PAGE_INFO Active Directory
topic_type:
- apiref
api_name:
- DSA_SEC_PAGE_INFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 26fa3dcfb983de8e1052b319bac7c3a594e256b594847c32b553353e6caee17d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695647"
---
# <a name="dsa_sec_page_info-structure"></a>Structure des informations de la \_ page DSA sec \_ \_

La structure des informations de la **\_ \_ page \_ DSA s** est utilisée avec les feuilles de propriétés [**WM \_ ADSPROP \_ \_**](wm-adsprop-sheet-create.md) et [**WM \_ DSA \_ \_ créer \_**](wm-dsa-sheet-create-notify.md) des messages Notify pour définir une feuille de propriétés secondaire dans un composant logiciel enfichable MMC Active Directory.

> [!Note]  
> Cette structure n’est pas définie dans un fichier d’en-tête publié. Pour utiliser cette structure, définissez-la dans le format exact indiqué.

 

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _DSA_SEC_PAGE_INFO {
  HWND          hwndParentSheet;
  DWORD         offsetTitle;
  DSOBJECTNAMES dsObjectNames;
} DSA_SEC_PAGE_INFO, *PDSA_SEC_PAGE_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**hwndParentSheet**
</dt> <dd>

Contient le handle de fenêtre du parent de la feuille de propriétés secondaire.

</dd> <dt>

**offsetTitle**
</dt> <dd>

Contient l’offset, en octets, entre le début de la structure des informations de la **\_ \_ page \_ DSA s** et une chaîne Unicode terminée par le caractère null qui contient le titre de la feuille de propriétés secondaire.

</dd> <dt>

**dsObjectNames**
</dt> <dd>

Contient une structure [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) qui définit la feuille de propriétés secondaire. Une seule feuille de propriétés secondaire peut être créée à la fois, de sorte que la structure **DSOBJECTNAMES** ne peut contenir qu’une seule structure [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**création de la \_ feuille ADSPROP WM \_ \_**](wm-adsprop-sheet-create.md)
</dt> <dt>

[**créer une notification de la \_ feuille DSA DSA \_ \_ \_**](wm-dsa-sheet-create-notify.md)
</dt> <dt>

[**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> </dl>

 

 





