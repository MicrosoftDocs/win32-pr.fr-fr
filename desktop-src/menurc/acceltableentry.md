---
title: ACCELTABLEENTRY, structure
description: Décrit les données dans une ressource de table d’accélérateurs individuelle. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.
ms.assetid: 510594ae-56ea-49fb-abd3-ec06e51f2e0e
keywords:
- Menus de la structure ACCELTABLEENTRY et autres ressources
topic_type:
- apiref
api_name:
- ACCELTABLEENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9ff12fe39f2ea54c90530133263bceb157d79dcf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412865"
---
# <a name="acceltableentry-structure"></a>ACCELTABLEENTRY, structure

Décrit les données dans une ressource de table d’accélérateurs individuelle. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  WORD fFlags;
  WORD wAnsi;
  WORD wId;
  WORD padding;
} ACCELTABLEENTRY;
```



## <a name="members"></a>Membres

<dl> <dt>

**fFlags**
</dt> <dd>

Type : **Word**

</dd> <dd>

Décrit les caractéristiques des accélérateurs clavier. Ce membre peut avoir une ou plusieurs des valeurs suivantes de winuser. h.



| Valeur                                                                                                                                                                                                      | Signification                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVIRTKEY"></span><span id="fvirtkey"></span><dl> <dt>**FVIRTKEY**</dt> <dt>true</dt> </dl>    | La touche accélérateur est un [Code de touche virtuelle](/windows/desktop/inputdev/virtual-key-codes). Si cet indicateur n’est pas spécifié, la touche d’accès rapide est supposée spécifier un code de caractère ASCII. <br/>                          |
| <span id="FNOINVERT"></span><span id="fnoinvert"></span><dl> <dt>**FNOINVERT**</dt> <dt>0x02</dt> </dl> | Un élément de menu de la barre de menus n’est pas mis en surbrillance lorsqu’un accélérateur est utilisé. Cet attribut est obsolète et conservé uniquement à des fins de compatibilité descendante avec les fichiers de ressources conçus pour une Windows 16 bits.<br/> |
| <span id="FSHIFT"></span><span id="fshift"></span><dl> <dt>**FSHIFT**</dt> <dt>0x04</dt> </dl>          | L’accélérateur est activé uniquement si l’utilisateur appuie sur la touche Maj. Cet indicateur s’applique uniquement aux clés virtuelles. <br/>                                                                                        |
| <span id="FCONTROL"></span><span id="fcontrol"></span><dl> <dt>**FCONTROL**</dt> <dt>0x08</dt> </dl>    | L’accélérateur est activé uniquement si l’utilisateur appuie sur la touche CTRL. Cet indicateur s’applique uniquement aux clés virtuelles. <br/>                                                                                         |
| <span id="FALT"></span><span id="falt"></span><dl> <dt>**Falt**</dt> <dt>0x10</dt> </dl>                | L’accélérateur est activé uniquement si l’utilisateur appuie sur la touche ALT. Cet indicateur s’applique uniquement aux clés virtuelles. <br/>                                                                                          |
| <span id="0x80"></span><span id="0X80"></span><dl> <dt>**0x80**</dt> </dl>                                                                          | L’entrée est la dernière dans une table d’accélérateurs. <br/>                                                                                                                                                          |



 

</dd> <dt>

**wAnsi**
</dt> <dd>

Type : **Word**

</dd> <dd>

Valeur de caractère ANSI ou code de touche virtuelle qui identifie la touche accélérateur.

</dd> <dt>

**wId**
</dt> <dd>

Type : **Word**

</dd> <dd>

Identificateur de l’accélérateur clavier. Il s’agit de la valeur passée à la procédure de fenêtre lorsque l’utilisateur appuie sur la touche spécifiée.

</dd> <dt>

**padding**
</dt> <dd>

Type : **Word**

</dd> <dd>

Nombre d’octets insérés pour garantir que la structure est alignée sur une limite **DWORD** .

</dd> </dl>

## <a name="remarks"></a>Notes

La structure **ACCELTABLEENTRY** est répétée pour toutes les entrées de la table d’accélérateurs dans la ressource. La dernière entrée de la table est marquée avec la valeur 0x0080.

Vous pouvez calculer le nombre d’éléments dans la table si vous divisez la longueur de la ressource par huit. Ensuite, votre application peut accéder de manière aléatoire aux entrées de longueur fixe individuelles.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Ressources](resources.md)
</dt> </dl>

 

