---
description: la méthode OpenModule de l’objet merge ouvre un module de fusion Windows Installer en mode lecture seule. Vous devez ouvrir un module avant de pouvoir le fusionner avec une base de données d’installation.
ms.assetid: fc976899-2c39-4314-b2fb-417e0dfc53b9
title: Merge. OpenModule, méthode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenModule
- IMsmMerge.OpenModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9d83a9331c91817f70c49ecf74c7171c5e627be6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413974"
---
# <a name="mergeopenmodule-method"></a>Merge. OpenModule, méthode

la méthode **OpenModule** de l’objet [**merge**](merge-object.md) ouvre un module de fusion Windows Installer en mode lecture seule. Vous devez ouvrir un module avant de pouvoir le fusionner avec une base de données d’installation.

## <a name="syntax"></a>Syntaxe


```JScript
Merge.OpenModule(
  FileName,
  Language
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FileName* 
</dt> <dd>

Nom de fichier complet pointant vers un module de fusion.

</dd> <dt>

*Langage* 
</dt> <dd>

Identificateur de langue valide (LANGID).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette fonction ouvre le module de fusion en mode lecture seule et exclut l’écriture d’autres programmes dans le module de fusion jusqu’à ce que la méthode [**CloseModule**](merge-closemodule.md) soit appelée.

Le programme d’installation tente d’ouvrir le module dans la langue spécifiée par la *langue*, ou dans une langue plus générale. Par exemple, si la *langue* est spécifiée comme 1033, un module avec une langue par défaut de 1033, 9 ou 0 peut être ouvert dans sa langue par défaut. La valeur de *langue* 9 ouvre les modules dont la langue par défaut est 9 ou 0. Si la langue par défaut du module ne répond pas aux exigences spécifiées, une tentative est faite pour transformer le module en la langue demandée. En cas d’échec, le module est transformé en langages de plus en plus généraux, tout comme le langage neutre. Si aucune des transformations ne réussit, le module ne parvient pas à s’ouvrir. Dans ce cas, une erreur est ajoutée à la liste d’erreurs de type msmErrorLanguageUnsupported. En cas d’erreur lors de la transformation du module en langue souhaitée, une erreur est ajoutée à la liste d’erreurs de type msmErrorLanguageFailed. Pour plus d’informations, consultez la propriété [**type**](error-type.md) de l’objet [**Error**](error-object.md) . L’ouverture d’un module de fusion efface toutes les erreurs qui n’ont pas encore été récupérées.

### <a name="c"></a>C++

Consultez fonction [**OpenModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
