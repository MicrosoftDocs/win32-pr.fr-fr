---
title: WMDMRIGHTS, structure
description: La structure WMDMRIGHTS décrit les droits d’utilisation de contenu.
ms.assetid: 1be9167b-0d20-4a17-a42b-9696ada2b539
keywords:
- Structure WMDMRIGHTS Windows Media Gestionnaire de périphériques
- Pointeur de structure PWMDMRIGHTS Windows Media Gestionnaire de périphériques
topic_type:
- apiref
api_name:
- WMDMRIGHTS
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8bc3bcd61efc64d32daa3179b77a9aaa518d4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535864"
---
# <a name="wmdmrights-structure"></a>WMDMRIGHTS, structure

La structure **WMDMRIGHTS** décrit les droits d’utilisation de contenu.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct __WMDMRIGHTS {
  UINT         cbSize;
  DWORD        dwContentType;
  DWORD        fuFlags;
  DWORD        fuRights;
  DWORD        dwAppSec;
  DWORD        dwPlaybackCount;
  WMDMDATETIME ExpirationDate;
} WMDMRIGHTS, *PWMDMRIGHTS;
```



## <a name="members"></a>Membres

<dl> <dt>

**cbSize**
</dt> <dd>

Taille de la structure en octets.

</dd> <dt>

**dwContentType**
</dt> <dd>

**Valeur DWORD** contenant le type de contenu.

</dd> <dt>

**fuFlags**
</dt> <dd>

Champ de bits spécifiant les options de droits en cours d’utilisation pour le contenu.



| Valeur                        | Description                                  |
|------------------------------|----------------------------------------------|
| WMDM \_ droits \_ PLAYBACKCOUNT  | Nombre de fois où le fichier peut être lu. |
| WMDM- \_ droits \_ EXPIRATIONDATE | Date d’expiration du fichier.                 |
| WMDM \_ droits \_ FREESERIALIDS  | Identificateur de série gratuit du fichier.          |
| WMDM \_ \_ groupe GROUPID de droits  | Identificateur du fichier.                      |
| WMDM \_ droits \_ NAMEDSERIALIDS | Identificateur de série nommé du fichier.         |



 

</dd> <dt>

**fuRights**
</dt> <dd>

Champ de bits contenant les bits de droits pour le contenu.



| Valeur                                     | Description                                   |
|-------------------------------------------|-----------------------------------------------|
| WMDM \_ les \_ droits \_ de lecture sur le \_ PC                | Le contenu peut être lu sur un ordinateur personnel. |
| WMDM \_ copier les droits \_ \_ sur un \_ \_ appareil non SDMI \_ | Le contenu peut être copié sur un appareil non-SDMI.   |
| \_copier les droits WMDM \_ \_ sur \_ CD                | Le contenu peut être copié sur un CD.                |
| \_copier les droits WMDM sur l' \_ \_ \_ \_ appareil SDMI      | Le contenu peut être copié sur un appareil SDMI.      |



 

</dd> <dt>

**dwAppSec**
</dt> <dd>

Tableau d’octets qui spécifie le niveau minimal de sécurité de l’application.

</dd> <dt>

**dwPlaybackCount**
</dt> <dd>

**Valeur DWORD** qui contient le nombre de fois où le contenu peut être rendu.

</dd> <dt>

**ExpirationDate**
</dt> <dd>

Structure [**WMDMDATETIME**](wmdmdatetime.md) contenant la date et l’heure d’expiration du contenu. Si la licence n’a pas de date d’expiration, le membre **wYear** a la valeur 0xFFFF et tous les autres membres de **WMDMDATETIME** sont ignorés.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMDSPStorage :: GetRight**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getrights)
</dt> <dt>

[**IWMDMStorage :: GetRight**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getrights)
</dt> <dt>

[**WMDMDATETIME**](wmdmdatetime.md)
</dt> <dt>

[**Structures**](structures.md)
</dt> </dl>

 

 





