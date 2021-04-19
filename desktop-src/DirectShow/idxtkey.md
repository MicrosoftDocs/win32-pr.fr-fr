---
description: L’interface IDxtKey définit les propriétés de la transition de clé. Cette interface est utilisée en interne par les services de modification DirectShow (DES) lors du rendu de la transition de clé.
ms.assetid: b929bf0c-8aaf-456e-b692-e23d88e480dd
title: Interface IDxtKey (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f4f1bc6a5dd0e89789e098fc4180bfc826f10c93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538774"
---
# <a name="idxtkey-interface"></a>Interface IDxtKey

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L' `IDxtKey` interface définit les propriétés de la transition de [clé](key-transition.md) .

Cette interface est utilisée en interne par les services de modification DirectShow (DES) lors du rendu de la transition de clé. Les applications DES n’ont pas besoin d’utiliser cette interface. Pour définir les propriétés d’une transition dans DES, utilisez l’interface [**IPropertySetter**](ipropertysetter.md) .

## <a name="members"></a>Membres

L’interface **IDxtKey** hérite de **IDXEffect**. **IDxtKey** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IDxtKey** possède ces méthodes.



| Méthode                                            | Description                                                                            |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**Obtient la \_ teinte**](idxtkey-get-hue.md)               | Récupère la valeur de teinte sur laquelle la clé doit être ajoutée.<br/>                                    |
| [**être \_ inversée**](idxtkey-get-invert.md)         | Récupère une valeur booléenne indiquant si l’opération de clé est inversée.<br/> |
| [**Obtient le \_ KeyType**](idxtkey-get-keytype.md)       | Récupère le type de clé.<br/>                                                  |
| [**récupérer de la \_ luminance**](idxtkey-get-luminance.md)   | Récupère la valeur de luminance sur laquelle la clé doit être ajoutée.<br/>                              |
| [**recevoir des \_ couleurs RVB**](idxtkey-get-rgb.md)               | Récupère la couleur RVB sur laquelle la touche est enfoncée.<br/>                                    |
| [**faire \_ la similarité**](idxtkey-get-similarity.md) | Récupère la plage de données de couleur qui devient transparente.<br/>                 |
| [**mettre la \_ teinte**](idxtkey-put-hue.md)               | Spécifie la valeur de teinte sur laquelle la clé doit être ajoutée.<br/>                                    |
| [**mettre en \_ inverse**](idxtkey-put-invert.md)         | Spécifie si l’opération de clé est inversée.<br/>                            |
| [**Placer le \_ KeyType**](idxtkey-put-keytype.md)       | Spécifie le type de clé.<br/>                                                  |
| [**Placer la \_ luminance**](idxtkey-put-luminance.md)   | Spécifie la valeur de luminance sur laquelle la clé doit être ajoutée.<br/>                              |
| [**mettre en \_ RVB**](idxtkey-put-rgb.md)               | Spécifie la couleur RVB sur laquelle la clé doit être représentée.<br/>                                    |
| [**similarité des mises en place \_**](idxtkey-put-similarity.md) | Spécifie la plage de données de couleur qui devient transparente.<br/>                 |



 

## <a name="remarks"></a>Notes

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 




