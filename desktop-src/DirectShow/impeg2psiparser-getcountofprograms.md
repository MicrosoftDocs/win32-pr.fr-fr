---
description: 'IMpeg2PsiParser :: GetCountOfPrograms, méthode-l’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow. Il ne s’agit pas d’une API DirectShow prise en charge.'
ms.assetid: 282dd779-9aca-46e3-a791-cb9ea86f637d
title: 'IMpeg2PsiParser :: GetCountOfPrograms, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfPrograms
api_type:
- COM
api_location: ''
ms.openlocfilehash: d6bfe698a45ea1cfe0a4bac6e65b839292bc1996
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119427"
---
# <a name="impeg2psiparsergetcountofprograms-method"></a>IMpeg2PsiParser :: GetCountOfPrograms, méthode

L’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow. Il ne s’agit pas d’une API DirectShow prise en charge.

La `GetCountOfPrograms` méthode récupère le nombre de programmes dans le flux de transport.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCountOfPrograms(
  [out] int *pNumOfPrograms
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pNumOfPrograms* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre de programmes.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

La méthode retourne une valeur HRESULT. Les valeurs possibles sont, sans s’y limiter, les valeurs indiquées dans le tableau suivant.



| Code de retour                                                                          | Description         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Réussite.<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IMpeg2PsiParser**](impeg2psiparser.md)
</dt> <dt>

[Exemple de filtre de l’analyseur PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




