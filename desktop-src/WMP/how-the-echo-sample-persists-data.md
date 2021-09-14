---
title: Comment l’exemple Echo conserve les données
description: Comment l’exemple Echo conserve les données
ms.assetid: be75760f-c378-45d1-99de-43ef0ec4b8f0
keywords:
- plug-ins Lecteur Windows Media, pages de propriétés de l’exemple Echo
- plug-ins, pages de propriétés d’exemple Echo
- plug-ins de traitement de signal numérique, pages de propriétés d’exemple Echo
- Plug-ins DSP, pages de propriétés d’exemple Echo
- Exemple de plug-in DSP Echo, pages de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df781754fd52639272850158187cb1258c081583
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416234"
---
# <a name="how-the-echo-sample-persists-data"></a>Comment l’exemple Echo conserve les données

lorsque Lecteur Windows Media active un plug-in DSP, il peut créer et détruire de nombreuses instances de l’objet de plug-in au cours d’une session. Le plug-in a besoin d’un moyen de conserver ses valeurs de propriété entre les instances. l’exemple de code généré par l’assistant de Plug-in Lecteur Windows Media stocke ces valeurs dans le registre et les récupère lorsque la page de propriétés est appelée ou lorsqu’une nouvelle instance du Plug-in est créée.

L’exemple de code par défaut dans Echo. h comprend deux constantes qui stockent le chemin d’accès au registre par défaut et la chaîne de nom du facteur d’échelle. Vous devez conserver la variable qui spécifie le chemin d’accès, mais supprimer la ligne qui spécifie le nom du Registre du facteur d’échelle. Ensuite, ajoutez le code suivant pour définir des constantes pour les noms de propriétés de délai d’attente et de combinaison humide dans le registre. La section terminé doit se présenter comme suit :


```C++
// registry location for preferences
const TCHAR kszPrefsRegKey[] = _T("Software\\Echo\\DSP Plugin");
const TCHAR kszPrefsDelayTime[] = _T("DelayTime");
const TCHAR kszPrefsWetmix[] = _T("Wetmix");

```



Vous allez utiliser ces constantes lorsque vous modifiez les méthodes de la page de propriétés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Modification de la page de propriétés de l’exemple Echo**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




