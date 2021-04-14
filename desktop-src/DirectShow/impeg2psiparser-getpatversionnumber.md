---
description: L’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow. Il ne s’agit pas d’une API DirectShow prise en charge.
ms.assetid: 2f5ad9bf-3d70-491a-ab45-15cd922a02d4
title: 'IMpeg2PsiParser :: GetPatVersionNumber, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPatVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6117060cf0c8d3c56d03e5838376485244fde8d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392448"
---
# <a name="impeg2psiparsergetpatversionnumber-method"></a>IMpeg2PsiParser :: GetPatVersionNumber, méthode

L’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow. Il ne s’agit pas d’une API DirectShow prise en charge.

La `GetPatVersionNumber` méthode récupère le champ du \_ numéro de version à partir de Pat. Un flux de transport contient au plus un PAT. Le numéro de version est incrémenté chaque fois que les informations de la table sont modifiées.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetPatVersionNumber(
  [out] BYTE *pPatVersion
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pPatVersion* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le champ du numéro de version \_ .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne une valeur **HRESULT** . Les valeurs possibles sont, sans s’y limiter, les valeurs indiquées dans le tableau suivant.



| Code de retour                                                                          | Description         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Opération réussie.<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IMpeg2PsiParser**](impeg2psiparser.md)
</dt> <dt>

[Exemple de filtre de l’analyseur PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




