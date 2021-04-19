---
description: La méthode FindMediaFile recherche un fichier et, en cas de réussite, récupère le chemin d’accès au fichier.
ms.assetid: ddfa2c75-e51f-4aad-afe6-8a60c46e8d35
title: 'IMediaLocator :: FindMediaFile, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator.FindMediaFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3561b77873c90b2d4bd0202bed8e2da822a0362f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528018"
---
# <a name="imedialocatorfindmediafile-method"></a>IMediaLocator :: FindMediaFile, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `FindMediaFile` méthode recherche un fichier et, en cas de réussite, récupère le chemin d’accès au fichier.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT FindMediaFile(
   BSTR Input,
   BSTR FilterString,
   BSTR *pOutput,
   long Flags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Entrée* 
</dt> <dd>

Nom du fichier, y compris le chemin d’accès, où le fichier a été connu pour la dernière fois. Pour les objets source de la chronologie, utilisez le nom du support actuel.

</dd> <dt>

*FilterString* 
</dt> <dd>

**BSTR** contenant des paires de chaînes de filtre, au format requis par le membre **lpstrFilter** de la structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) . Le localisateur de média utilise ce filtre s’il affiche une boîte de dialogue Ouvrir un fichier. La valeur peut être **null** si le paramètre *Flags* n’inclut pas l' \_ \_ indicateur Popup SFN VALIDATEF.

</dd> <dt>

*pOutput* 
</dt> <dd>

Pointeur vers une variable qui reçoit le chemin d’accès réel au fichier, s’il diffère de la valeur contenue dans l' *entrée* et si la méthode parvient à localiser le fichier.

</dd> <dt>

*Indicateurs* 
</dt> <dd>

Combinaison d’opérations de bits de zéro ou plusieurs indicateurs. Pour obtenir la liste des indicateurs possibles, consultez [**indicateurs de validation du nom de fichier**](file-name-validation-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

La chaîne de filtre de la boîte de dialogue d’ouverture de fichier, qui est spécifiée par le paramètre *FilterString* , contient des caractères null internes. Par exemple, Video \\ 0 \* . avi \\ 0 \\ 0 est une chaîne de filtre valide. Vous ne pouvez pas utiliser la fonction **SysAllocStr** pour allouer le BSTR, car cette fonction attend une chaîne terminée par le caractère null et va tronquer la chaîne au premier caractère null. Par conséquent, utilisez une fonction telle que **SysAllocStringLen**, qui comprend un paramètre explicite pour la longueur :


```C++
BSTR filter = SysAllocStringLen(L"Video\0*.avi\0", 12);
// Note: SysAllocStringLen appends an additional '\0' to the string.
```



Si l’utilisateur annule la boîte de dialogue d’ouverture de fichier, la méthode renvoie E \_ Fail.

La méthode alloue de la mémoire pour le **BSTR** dans *pOutput*. L’application doit appeler **SysFreeString** pour libérer la mémoire.

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IMediaLocator**](imedialocator.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 
