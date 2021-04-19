---
description: La méthode SetSourceNameValidation spécifie la manière dont le moteur de rendu valide les noms de fichiers.
ms.assetid: b33904cd-ed7d-41b5-9ebf-50983ec9f7b3
title: 'IRenderEngine :: SetSourceNameValidation, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetSourceNameValidation
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 96164a817fd04f505b32c17be1bff3268e847df8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543267"
---
# <a name="irenderenginesetsourcenamevalidation-method"></a>IRenderEngine :: SetSourceNameValidation, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `SetSourceNameValidation` méthode spécifie la manière dont le moteur de rendu valide les noms de fichiers.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetSourceNameValidation(
   BSTR          FilterString,
   IMediaLocator *pOverride,
   LONG          Flags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FilterString* 
</dt> <dd>

Valeur **BSTR** contenant des paires de chaînes de filtre, au format requis par le membre **lpstrFilter** de la structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) . Le localisateur de média utilise ce filtre s’il présente une boîte de dialogue Ouvrir un fichier à l’utilisateur final.

</dd> <dt>

*pOverride* 
</dt> <dd>

Pointeur facultatif vers l’interface [**IMediaLocator**](imedialocator.md) d’un localisateur de média à utiliser à la place de la valeur par défaut. Pour utiliser le localisateur de média par défaut, affectez la valeur **null** à ce paramètre. Pour plus d'informations, consultez la section Notes.

</dd> <dt>

*Indicateurs* 
</dt> <dd>

Combinaison d’opérations de bits des [**indicateurs de validation de nom de fichier**](file-name-validation-flags.md) spécifiant le comportement du localisateur de média. L' \_ indicateur de vérification SFN VALIDATEF \_ doit être présent. L' \_ indicateur SFN VALIDATEF \_ hlinkMUTED n’a aucun effet avec cette méthode.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** suivantes :



| Code de retour                                                                                            | Description                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | Opération réussie.<br/>                            |
| <dl> <dt>**E \_ doit \_ initialiser le \_ convertisseur**</dt> </dl> | Le moteur de rendu n’a pas pu s’initialiser.<br/> |



 

## <a name="remarks"></a>Notes

À l’aide du paramètre *pOverride* , vous pouvez fournir votre propre implémentation personnalisée de l’interface [**IMediaLocator**](imedialocator.md) . Par exemple, le localisateur de média par défaut n’avertit pas une application des fichiers qu’elle trouve (ou ne peut pas trouver). Pour contourner cette limitation, vous pouvez implémenter un localisateur de média personnalisé, ce qui en fait un wrapper pour la version par défaut. Ensuite, transmettez [**IMediaLocator :: FindMediaFile**](imedialocator-findmediafile.md) appelle directement à la version par défaut et examinez la valeur de retour.

Actuellement, cette méthode ne valide pas les sources chargées dynamiquement. Consultez [**IRenderEngine :: SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).

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

[**Interface IRenderEngine**](irenderengine.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 
