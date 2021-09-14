---
title: External. NavigateTaskPaneURL, méthode
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. NavigateTaskPaneURL, méthode
ms.assetid: c3a888c0-6589-4d21-9d47-37372d9069f4
keywords:
- Lecteur Windows Media de la méthode NavigateTaskPaneURL
- méthode NavigateTaskPaneURL Lecteur Windows Media, classe externe
- Lecteur Windows Media de classe externe, méthode NavigateTaskPaneURL
topic_type:
- apiref
api_name:
- External.NavigateTaskPaneURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e70558c7616738f67d9dc1d6d29eca15e5c30d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192379"
---
# <a name="externalnavigatetaskpaneurl-method"></a>External. NavigateTaskPaneURL, méthode

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

La méthode **NavigateTaskPaneURL** ouvre une page Web dans le volet de tâches spécifié et active le volet spécifié.

## <a name="syntax"></a>Syntaxe


```JScript
External.NavigateTaskPaneURL(
  bstrKeyName,
  bstrTaskPane,
  bstrParams
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrKeyName* \[ dans\]
</dt> <dd>

**Chaîne** contenant le nom de clé du magasin en ligne. (obligatoire)

</dd> <dt>

*bstrTaskPane* \[ dans\]
</dt> <dd>

**Chaîne** contenant le nom du volet de tâches dans lequel la page Web s’ouvre. (obligatoire)

</dd> <dt>

*bstrParams* \[ dans\]
</dt> <dd>

**Chaîne** contenant les paramètres de chaîne de requête à ajouter à l’URL spécifiée par l’élément **Navigate** du document serviceInfo. (facultatif)

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La navigation vers un volet que votre magasin en ligne ne prend pas en charge peut entraîner la modification du magasin en ligne actuel.

La valeur spécifiée pour *bstrParams* est valide uniquement lorsque **NavigateTaskPaneURL** est appelé à partir de pages Web fournies par le magasin en ligne.

Le tableau suivant répertorie les valeurs valides pour *bstrTaskPane* et le volet de tâches associé pour chacun d’entre eux.



| Valeur            | Volet des tâches                      |
|------------------|--------------------------------|
| **ServiceTask1** | Premier volet de tâches du magasin en ligne.  |
| **ServiceTask2** | Deuxième volet des tâches du magasin en ligne. |
| **ServiceTask3** | Troisième volet des tâches de la boutique en ligne.  |



 

Votre code de page Web doit spécifier une valeur pour [External. SelectedTaskPane](external-selectedtaskpane.md) lors du chargement pour garantir que le bouton de volet de tâches correct est mis en surbrillance une fois la navigation terminée.

## <a name="examples"></a>Exemples

L’exemple de code suivant montre comment **NavigateTaskPaneURL** crée l’URL de la page Web à afficher pour **ServiceTask1**.

Exemple de l’élément **Navigate** :


```XML
<Navigate
    BaseURL = "https://www.proseware.com/online store/html/navigate.asp">
</Navigate>
```



Exemple d’appel à la méthode **NavigateTaskPaneURL** :


```XML
external.NavigateTaskPaneURL("Proseware", "ServiceTask1", "Pane=Store");
```



Exemple d’URL résultante utilisée pour la page Web affichée dans **ServiceTask1**:


```XML
https://www.proseware.com/online store/html/navigate.asp?Pane=Store
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 10 ou version ultérieure<br/>                                        |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet externe pour les magasins de type 2 en ligne**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**External. SelectedTaskPane**](external-selectedtaskpane.md)
</dt> </dl>

 

 





