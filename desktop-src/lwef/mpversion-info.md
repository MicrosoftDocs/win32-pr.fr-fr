---
title: Structure MPVERSION_INFO (MpClient. h)
description: Informations de version pour les composants du gestionnaire de protection contre les programmes malveillants.
ms.assetid: C18EE6FE-57E1-4814-85CA-19C3ACE275D2
keywords:
- fonctionnalités d’environnement Windows héritées de la structure MPVERSION_INFO
- PMPVERSION_INFO des fonctionnalités d’environnement du pointeur de structure Windows hérité
topic_type:
- apiref
api_name:
- MPVERSION_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50a89b03b8b310416f9b0b496c055f732f4e83859bb7eba50b7891abebc27d26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608699"
---
# <a name="mpversion_info-structure"></a>\_Structure d’informations MPVERSION

Informations de version pour les composants du gestionnaire de protection contre les programmes malveillants.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPVERSION_INFO {
  MPCOMPONENT_VERSION Product;
  MPCOMPONENT_VERSION Service;
  MPCOMPONENT_VERSION FileSystemFilter;
  MPCOMPONENT_VERSION Engine;
  MPCOMPONENT_VERSION ASSignature;
  MPCOMPONENT_VERSION AVSignature;
  MPCOMPONENT_VERSION NISEngine;
  MPCOMPONENT_VERSION NISSignature;
  MPCOMPONENT_VERSION Reserved[4];
} MPVERSION_INFO, *PMPVERSION_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**Produit**
</dt> <dd>

Type : **[ **MPCOMPONENT \_ version**](mpcomponent-version.md)**

</dd> <dd>

Version du produit.

</dd> <dt>

**Service**
</dt> <dd>

Type : **[ **MPCOMPONENT \_ version**](mpcomponent-version.md)**

</dd> <dd>

Version du composant du service.

</dd> <dt>

**FileSystemFilter**
</dt> <dd>

Type : **[ **MPCOMPONENT \_ version**](mpcomponent-version.md)**

</dd> <dd>

Version du composant filtre du système de fichiers.

</dd> <dt>

**Moteur**
</dt> <dd>

Type : **[ **MPCOMPONENT \_ version**](mpcomponent-version.md)**

</dd> <dd>

Version du composant moteur.

</dd> <dt>

**ASSignature**
</dt> <dd>

Type : **[ **MPCOMPONENT \_ version**](mpcomponent-version.md)**

</dd> <dd>

Version du composant de signature anti-espion.

</dd> <dt>

**AVSignature**
</dt> <dd>

Type : **[ **MPCOMPONENT \_ version**](mpcomponent-version.md)**

</dd> <dd>

Version du composant de signature antivirus.

</dd> <dt>

**NISEngine**
</dt> <dd>

Type : **[ **MPCOMPONENT \_ version**](mpcomponent-version.md)**

</dd> <dd>

Version du moteur NIS.

</dd> <dt>

**NISSignature**
</dt> <dd>

Type : **[ **MPCOMPONENT \_ version**](mpcomponent-version.md)**

</dd> <dd>

Version du composant de signature de signature NIS.

</dd> <dt>

**Reserved**
</dt> <dd>

Type : **[**MPCOMPONENT \_ version**](mpcomponent-version.md) \[ 4\]**

</dd> <dd>

Champs réservés.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**VERSION de MPCOMPONENT \_**](mpcomponent-version.md)
</dt> </dl>

 

 





