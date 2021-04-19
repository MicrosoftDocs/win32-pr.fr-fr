---
description: La méthode GetFilterGraph récupère le graphique de filtre que le moteur de rendu a construit, le cas échéant.
ms.assetid: 509b2c9c-c21b-4855-880f-f09ad342e758
title: 'IRenderEngine :: GetFilterGraph, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetFilterGraph
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c4750e6127c0d57758e46b2309f4d91afc110e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530283"
---
# <a name="irenderenginegetfiltergraph-method"></a>IRenderEngine :: GetFilterGraph, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `GetFilterGraph` méthode récupère le graphique de filtre que le moteur de rendu a construit, le cas échéant.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetFilterGraph(
  [out] IGraphBuilder **ppFG
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppFG* \[ à\]
</dt> <dd>

Reçoit un pointeur vers l’interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) du graphique de filtre. Elle reçoit la valeur **null** s’il n’existe aucun graphique de filtre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** suivantes :



| Code de retour                                                                                            | Description                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | Opération réussie.<br/>                            |
| <dl> <dt>**E \_ doit \_ initialiser le \_ convertisseur**</dt> </dl> | Le moteur de rendu n’a pas pu s’initialiser.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl>              | Pointeur non valide.<br/>                    |



 

## <a name="remarks"></a>Notes

Utilisez la méthode [**IRenderEngine :: ConnectFrontEnd**](irenderengine-connectfrontend.md) pour créer le serveur frontal du graphique de filtre. Pour la version préliminaire, utilisez [**IRenderEngine :: RenderOutputPins**](irenderengine-renderoutputpins.md) pour terminer le graphique. Pour la sortie de fichier, connectez le serveur frontal à une combinaison multiplexeur de fichiers/Mux. Pour plus d’informations, consultez [rendu d’un projet](rendering-a-project.md).

Le graphique résultant peut être exécuté, suspendu, arrêté et cherché ; Toutefois, la vitesse de lecture ne peut pas être modifiée.

En cas de retour, si la valeur de *\* ppFG* est non **null**, l’interface **IGraphBuilder** a un nombre de références en suspens. Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.

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

 

 




