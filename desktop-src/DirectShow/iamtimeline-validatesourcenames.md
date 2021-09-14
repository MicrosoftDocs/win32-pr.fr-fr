---
description: La méthode ValidateSourceNames valide les noms de sources dans la chronologie, à l’aide du localisateur de média. Si vous le souhaitez, cette méthode met également à jour tout objet source pour lequel il localise un fichier.
ms.assetid: 8f4b9ff0-f283-4bcb-83f4-92410cead7db
title: 'IAMTimeline :: ValidateSourceNames, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.ValidateSourceNames
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5154926cb9f814c94762b556721c7580e5b0d82c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857853"
---
# <a name="iamtimelinevalidatesourcenames-method"></a>IAMTimeline :: ValidateSourceNames, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `ValidateSourceNames` méthode valide les noms de sources dans la chronologie, à l’aide du localisateur de média. Si vous le souhaitez, cette méthode met également à jour tout objet source pour lequel il localise un fichier.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ValidateSourceNames(
   long          ValidateFlags,
   IMediaLocator *pOverride,
   long          NotifyEventHandle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ValidateFlags* 
</dt> <dd>

Combinaison d’opérations de bits des [**indicateurs de validation de nom de fichier**](file-name-validation-flags.md) spécifiant le comportement du localisateur de média. Les \_ indicateurs SFN VALIDATEF \_ Replace et SFN \_ VALIDATEF \_ Check doivent être présents, sinon la méthode renvoie E \_ INVALIDARG.

</dd> <dt>

*pOverride* 
</dt> <dd>

Pointeur facultatif vers l’interface [**IMediaLocator**](imedialocator.md) d’un localisateur de média à utiliser à la place de la valeur par défaut. Pour utiliser le localisateur de média par défaut, affectez la valeur **null** à ce paramètre. Pour plus d'informations, consultez la section Notes.

</dd> <dt>

*NotifyEventHandle* 
</dt> <dd>

Handle vers un événement. La méthode signale l’événement une fois la validation terminée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

À l’aide du paramètre *pOverride* , vous pouvez fournir votre propre implémentation personnalisée de l’interface [**IMediaLocator**](imedialocator.md) . Par exemple, le localisateur de média par défaut n’informe pas votre application des fichiers qu’il trouve (ou ne peut pas trouver). Pour contourner cette limitation, vous pouvez implémenter un localisateur de média personnalisé, ce qui en fait un wrapper pour la version par défaut. Dans votre version personnalisée, transmettez [**IMediaLocator :: FindMediaFile**](imedialocator-findmediafile.md) appelle directement à la version par défaut, puis examinez la valeur de retour.

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

[**Interface IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




