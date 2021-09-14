---
description: La méthode SetFilterGraph spécifie un graphique de filtre que le moteur de rendu utilise.
ms.assetid: 6a245864-7d22-4608-995b-b28662a6ab90
title: 'IRenderEngine :: SetFilterGraph, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetFilterGraph
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72c93ef6610fd301c497589858a8941e2b8f71b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126853714"
---
# <a name="irenderenginesetfiltergraph-method"></a>IRenderEngine :: SetFilterGraph, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `SetFilterGraph` méthode spécifie un graphique de filtre que le moteur de rendu utilise.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetFilterGraph(
   IGraphBuilder *pFG
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFG* 
</dt> <dd>

Pointeur vers l’interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) du graphique de filtre.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs **HRESULT** suivantes :



| Code de retour                                                                                            | Description                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | Réussite.<br/>                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Argument non valide.<br/>                   |
| <dl> <dt>**E \_ doit \_ initialiser le \_ convertisseur**</dt> </dl> | Le moteur de rendu n’a pas pu s’initialiser.<br/> |



 

## <a name="remarks"></a>Notes

La plupart des applications n’ont pas besoin d’appeler cette méthode. Il est plus courant de laisser le moteur de rendu générer le graphique pour vous, en appelant la méthode [**IRenderEngine :: ConnectFrontEnd**](irenderengine-connectfrontend.md) .

Cette méthode échoue si le moteur de rendu a déjà un graphique de filtre.

Ne récupérez jamais un pointeur vers un graphique de filtre créé par un moteur de rendu et utilisez-le en tant que paramètre de cette méthode sur un autre moteur de rendu. Cela entraînera des résultats imprévisibles.

la méthode **ConnectFrontEnd** détruit tout graphique de filtre existant, mais conserve la même instance de filtre Graph Manager.

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

 

 




