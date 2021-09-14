---
description: La méthode ConnectFrontEnd génère la partie frontale du graphique de filtre à partir de la chronologie actuelle.
ms.assetid: ac484fd6-b88d-4c3a-bc4d-f118083d706d
title: 'IRenderEngine :: ConnectFrontEnd, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.ConnectFrontEnd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 58ebd8e162f376b6ef942397e601139c46d8e4cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094718"
---
# <a name="irenderengineconnectfrontend-method"></a>IRenderEngine :: ConnectFrontEnd, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `ConnectFrontEnd` méthode génère la partie frontale du graphique de filtre à partir de la chronologie actuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ConnectFrontEnd();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** . Les valeurs de retour possibles sont les suivantes :



| Code de retour                                                                                                  | Description                                                                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                         | Réussite.<br/>                                                            |
| <dl> <dt>**\_OUTPUTRESET avertir \_**</dt> </dl>          | La partie de rendu du graphique a été supprimée.<br/>                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                 | Aucune chronologie n’est définie pour ce moteur de rendu.<br/>                             |
| <dl> <dt>**E \_ doit \_ initialiser le \_ convertisseur**</dt> </dl>       | Le moteur de rendu n’a pas pu s’initialiser.<br/>                                 |
| <dl> <dt>**le \_ moteur de rendu E \_ \_ est \_ défectueux**</dt> </dl> | L’opération a échoué, car le projet n’a pas été rendu correctement.<br/> |
| <dl> <dt>**E \_ inattendu**</dt> </dl>                 | Erreur inattendue.<br/>                                                   |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl>      | Type de média non valide.<br/>                                                 |



 

## <a name="remarks"></a>Notes

Cette méthode ne génère pas la partie de rendu du graphique de filtre. L’application doit connecter les broches de sortie du serveur frontal aux filtres de rendu souhaités :

-   Pour afficher un aperçu, appelez la méthode [**IRenderEngine :: RenderOutputPins**](irenderengine-renderoutputpins.md) .
-   Pour générer un fichier, appelez [**IRenderEngine :: GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) pour récupérer la broche de sortie de chaque groupe, puis connectez les broches à un filtre multiplexeur.

Si vous utilisez le moteur de rendu de base, les broches de sortie sur le serveur frontal produisent des données non compressées. Si vous utilisez le moteur de rendu intelligent, les broches de sortie produisent des données compressées.

Si vous modifiez la chronologie après avoir généré le graphique de filtre, vous devez à `ConnectFrontEnd` nouveau appeler pour reconstruire le serveur frontal. La méthode conserve la partie de rendu du graphique chaque fois que cela est possible. Toutefois, si vous ajoutez ou supprimez un groupe, ou si vous modifiez l’ordre des groupes, `ConnectFrontEnd` supprime la partie de rendu et votre application doit la reconstruire. Si la méthode supprime la partie de rendu, elle retourne S \_ WARN \_ OUTPUTRESET.

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

[**Interface IRenderEngine**](irenderengine.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




