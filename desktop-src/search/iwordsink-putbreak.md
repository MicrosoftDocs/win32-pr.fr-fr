---
description: Met un saut après le mot précédent.
ms.assetid: C8622067-D8CE-4099-8B9F-941720F4706B
title: IWordSink ::P méthode utBreak (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutBreak
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: c6407f1307b4860960c5202af13de736c7921139
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318149"
---
# <a name="iwordsinkputbreak-method"></a>IWordSink ::P méthode utBreak

Met un saut après le mot précédent.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT PutBreak(
  [in] WORDREP_BREAK_TYPE breakType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*breakType* \[ dans\]
</dt> <dd>

Valeur de [**\_ \_ type break WORDREP**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) qui indique le type de saut que le WordSink insère après le mot précédent. Chaque saut occupe une position unique dans l’index. Par conséquent, l’insertion de séparateurs entre les mots modifie la distance relative entre les mots.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                          | Description                                          |
|--------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | L’opération s’est terminée avec succès.<br/> |



 

## <a name="remarks"></a>Notes

Les méthodes [**IWordSinkPutWord**](iwordsink-putword.md) et [**IWordSink ::P utaltword**](iwordsink-putaltword.md) insèrent automatiquement une coupure de mot (EOW, indiquée par l' \_ élément WORDREP Break \_ EOW du type énuméré de [**\_ \_ type break WORDREP**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) ) après chaque mot. Appelez la méthode **PutBreak** pour insérer un type d’arrêt autre que la fin du mot. Cette méthode ne modifie pas la mémoire tampon de texte source (*pSourceText*) ou incrémente le nombre de caractères (*CWC*). Toutefois, elle incrémente la position actuelle dans l’index et affecte les résultats de la requête.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Rechercher. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IWordSink**](iwordsink.md)
</dt> </dl>

 

 
