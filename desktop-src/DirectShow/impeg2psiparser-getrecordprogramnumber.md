---
description: 'IMpeg2PsiParser :: GetRecordProgramNumber, méthode-l’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow. il ne s’agit pas d’une API DirectShow prise en charge.'
ms.assetid: 3800a0b1-a581-40ed-81ab-3d5f77f442df
title: 'IMpeg2PsiParser :: GetRecordProgramNumber, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetRecordProgramNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: e42e991fc7e288fc36dafcd167fe21ffb4983baeeb34bbb80e1bf67981e24779
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083699"
---
# <a name="impeg2psiparsergetrecordprogramnumber-method"></a>IMpeg2PsiParser :: GetRecordProgramNumber, méthode

l’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow. il ne s’agit pas d’une API DirectShow prise en charge.

La `GetRecordProgramNumber` méthode récupère le numéro de programme d’un programme spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetRecordProgramNumber(
  [in]  DWORD dwIndex,
  [out] WORD  *pwVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwIndex* \[ dans\]
</dt> <dd>

Spécifie l’entrée de la PAT qui définit le programme, indexée à partir de zéro.

</dd> <dt>

*pwVal* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le \_ champ de numéro de programme de la Pat.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne une valeur **HRESULT** . Les valeurs possibles sont, sans s’y limiter, les valeurs indiquées dans le tableau suivant.



| Code de retour                                                                          | Description         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Réussite.<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IMpeg2PsiParser**](impeg2psiparser.md)
</dt> <dt>

[Exemple de filtre de l’analyseur PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




