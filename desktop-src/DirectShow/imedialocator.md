---
description: l’interface IMediaLocator fournit des méthodes de validation des noms de fichiers dans DirectShow Services d’édition.
ms.assetid: 6c1ae957-a2be-454b-9451-772e4a670677
title: Interface IMediaLocator (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9664bf793e989c5975bcef0e712a550399c4ddee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126853797"
---
# <a name="imedialocator-interface"></a>Interface IMediaLocator

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

l' `IMediaLocator` interface fournit des méthodes de validation des noms de fichiers dans [DirectShow Services d’édition](directshow-editing-services.md) . Utilisez cette interface pour vous assurer qu’un nom de fichier et un chemin d’accès donnés correspondent à un fichier existant. Cette interface fournit également un moyen de rechercher le fichier à d’autres emplacements et d’afficher une boîte de dialogue **ouvrir** afin que l’utilisateur puisse localiser le fichier.

Le localisateur de média implémente cette interface. La chronologie et le moteur de rendu prennent également en charge la validation des noms de fichiers par le biais des méthodes suivantes :

-   [**IAMTimeline :: ValidateSourceNames**](iamtimeline-validatesourcenames.md): valide et met à jour les noms de fichiers dans la chronologie.
-   [**IRenderEngine :: SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md): spécifie la manière dont le moteur de rendu valide les noms de fichiers au moment du rendu.

En règle générale, une application DES appellera ces méthodes au lieu de créer directement une instance du localisateur de média. Pour plus d’informations, consultez [utilisation du localisateur de média](using-the-media-locator.md).

## <a name="members"></a>Membres

L’interface **IMediaLocator** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IMediaLocator** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IMediaLocator** possède ces méthodes.



| Méthode                                                     | Description                                                                        |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**AddFoundLocation**](imedialocator-addfoundlocation.md) | Ajoute un répertoire au cache de répertoire.<br/>                                |
| [**FindMediaFile**](imedialocator-findmediafile.md)       | Recherche un fichier et, en cas de réussite, récupère le chemin d’accès au fichier.<br/> |



 

## <a name="remarks"></a>Notes

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
