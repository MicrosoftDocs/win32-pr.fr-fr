---
description: La méthode LogError journalise une erreur. Les applications n’ont pas besoin d’appeler cette méthode. Elle est appelée en interne en réponse à des erreurs de rendu.
ms.assetid: 08765c8a-21ca-4c40-84a8-d13da87d9c5f
title: 'IAMErrorLog :: LogError, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMErrorLog.LogError
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dc94532639f325b53db850ebe8a5af489a8b3cf2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234144"
---
# <a name="iamerrorloglogerror-method"></a>IAMErrorLog :: LogError, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La méthode **LogError** journalise une erreur. Les applications n’ont pas besoin d’appeler cette méthode. Elle est appelée en interne en réponse à des erreurs de rendu.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT LogError(
       LONG    Severity,
       BSTR    ErrorString,
       LONG    ErrorCode,
       HRESULT hresult,
  [in] VARIANT *pExtraInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Gravité* 
</dt> <dd>

Réservé. Ne pas utiliser.

</dd> <dt>

*Telle* 
</dt> <dd>

Valeur de chaîne contenant le texte de l’erreur.

</dd> <dt>

*ErrorCode* 
</dt> <dd>

Code d’erreur.

</dd> <dt>

*signé* 
</dt> <dd>

Valeur HRESULT qui a été retournée par l’appel de méthode à l’origine de l’erreur.

</dd> <dt>

*pExtraInfo* \[ dans\]
</dt> <dd>

Pointeur vers un VARIANT qui contient des informations supplémentaires sur l’erreur.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la valeur du paramètre *HRESULT* .

## <a name="remarks"></a>Notes

Dans cette méthode, ne libérez pas la **variante** vers laquelle pointe *pExtraInfo*. En outre, la **variante** devient non valide après le retour de la méthode, donc n’essayez pas de la référencer ultérieurement.

Implémentez cette méthode pour retourner le plus rapidement possible. N’effectuez pas d’appels de fonction à l’intérieur de cette méthode qui peut bloquer l’exécution du programme. Par exemple, n’appelez pas les fonctions qui envoient des messages de fenêtre, bloquent les événements ou peuvent bloquer l’exécution. Cela peut entraîner le blocage de l’ordinateur.

Pour obtenir la liste des erreurs définies par DES, ainsi que la signification et le type de données de la **variante** vers laquelle pointe *PExtraInfo*, consultez [Erreurs de rendu](rendering-errors.md).

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IAMErrorLog**](iamerrorlog.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




