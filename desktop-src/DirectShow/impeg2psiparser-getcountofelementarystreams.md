---
description: L’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow. Il ne s’agit pas d’une API DirectShow prise en charge.
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
ms.openlocfilehash: 6593b699592c913940b14c2c26aea42057acfa40
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106543066"
---
# <a name="impeg2psiparsergetcountofelementarystreams-method"></a>IMpeg2PsiParser :: GetCountOfElementaryStreams, méthode

L’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow. Il ne s’agit pas d’une API DirectShow prise en charge.

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
| <dl> <dt>**\_OK**</dt> </dl> | Opération réussie.<br/> |



 

## <a name="remarks"></a>Notes

Utilisez la méthode **GetRecordProgramNumber** pour obtenir le numéro du programme.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IMpeg2PsiParser**](impeg2psiparser.md)
</dt> <dt>

[**IMpeg2PsiParser::GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[Exemple de filtre de l’analyseur PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




