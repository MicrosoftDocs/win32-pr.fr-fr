---
description: L’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow. Il ne s’agit pas d’une API DirectShow prise en charge.
ms.assetid: 50113d6b-4e10-4dc9-aaef-f67c6918a2de
title: 'IMpeg2PsiParser :: GetPmtVersionNumber, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPmtVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3af4b20067af52216181848f4cc63ac5a7784ba9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515738"
---
# <a name="impeg2psiparsergetpmtversionnumber-method"></a>IMpeg2PsiParser :: GetPmtVersionNumber, méthode

L’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow. Il ne s’agit pas d’une API DirectShow prise en charge.

La `GetPmtVersionNumber` méthode récupère le champ du \_ numéro de version à partir d’un PMT spécifié. Le numéro de version est incrémenté chaque fois que la définition du programme change.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetPmtVersionNumber(
  [in]  WORD wProgramNumber,
  [out] BYTE *pPmtVersion
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wProgramNumber* \[ dans\]
</dt> <dd>

Spécifie le \_ champ du numéro de programme du programme, comme indiqué dans le Pat.

</dd> <dt>

*pPmtVersion* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le champ du numéro de version \_ .

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

 

 




