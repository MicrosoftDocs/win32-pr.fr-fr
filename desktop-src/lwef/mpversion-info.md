---
title: Structure MPVERSION_INFO (MpClient. h)
description: Informations de version pour les composants du gestionnaire de protection contre les programmes malveillants.
ms.assetid: C18EE6FE-57E1-4814-85CA-19C3ACE275D2
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPVERSION_INFO
- PMPVERSION_INFO des fonctionnalités d’environnement Windows héritées du pointeur de structure
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
ms.openlocfilehash: f30153c427b880600a3d8aeb3c411a8679cd64b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317394"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**VERSION de MPCOMPONENT \_**](mpcomponent-version.md)
</dt> </dl>

 

 





