---
description: 'IMpeg2PsiParser :: GetCountOfElementaryStreams, méthode-l’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow. il ne s’agit pas d’une API DirectShow prise en charge.'
ms.assetid: 19ef96a8-3d5b-4da1-8cff-d6a271ad4915
title: 'IMpeg2PsiParser :: GetCountOfElementaryStreams, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfElementaryStreams
api_type:
- COM
api_location: ''
ms.openlocfilehash: e241697884a4b665c160dc9991e4cb7f02c76f1ba32bc7a0656515faf1117a58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767379"
---
# <a name="impeg2psiparsergetcountofelementarystreams-method"></a>IMpeg2PsiParser :: GetCountOfElementaryStreams, méthode

l’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow. il ne s’agit pas d’une API DirectShow prise en charge.

La `GetCountOfElementaryStreams` méthode récupère le nombre de flux élémentaires dans un programme spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCountOfElementaryStreams(
  [in]  WORD wProgramNumber,
  [out] WORD *pwVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wProgramNumber* \[ dans\]
</dt> <dd>

Spécifie le \_ champ du numéro de programme pour le programme, comme indiqué dans le Pat.

</dd> <dt>

*pwVal* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre de flux élémentaires dans le programme.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne une valeur **HRESULT** . Les valeurs possibles sont, sans s’y limiter, les valeurs indiquées dans le tableau suivant.



| Code de retour                                                                          | Description         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Réussite.<br/> |



 

## <a name="remarks"></a>Remarques

Utilisez la méthode **GetRecordProgramNumber** pour obtenir le numéro du programme.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IMpeg2PsiParser**](impeg2psiparser.md)
</dt> <dt>

[**IMpeg2PsiParser::GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[Exemple de filtre de l’analyseur PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




