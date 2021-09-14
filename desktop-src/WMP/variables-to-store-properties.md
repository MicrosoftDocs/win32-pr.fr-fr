---
title: Variables pour stocker les propriétés
description: Variables pour stocker les propriétés
ms.assetid: a90a6e21-00fb-46f8-96c8-654d8f205905
keywords:
- Lecteur Windows Media les plug-ins, exemples de propriétés Echo
- plug-ins, exemples de propriétés d’écho
- plug-ins de traitement de signal numérique, exemples de propriétés Echo
- Plug-ins DSP, exemples de propriétés Echo
- Echo DSP, exemple de plug-in, propriétés
- Echo DSP, exemple de plug-in, variables pour le stockage des propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d252962116ba9c72464273f9c4ea1688b151898
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010836"
---
# <a name="variables-to-store-properties"></a>Variables pour stocker les propriétés

Tout d’abord, vous aurez besoin d’une variable pour stocker le temps de retard. l’exemple par défaut créé par l’assistant de Plug-in Lecteur Windows Media fournit une variable nommée m \_ fScaleFactor pour stocker le multiplicateur de mise à l’échelle qu’il utilise pour le traitement. Cet exemple n’a plus besoin de cette variable. vous pouvez donc modifier son nom et son type pour stocker la valeur de délai.

1.  Remplacez chaque instance de m \_ fScaleFactor dans Echo. h et Echo. cpp par m \_ dwDelayTime.
2.  Remplacez le type de données de m \_ fScaleFactor (Now m \_ dwDelayTime) de double par DWORD dans Echo. h.
3.  Dans le constructeur de CEcho, remplacez la valeur de délai par défaut par 1000.
    ```C++
    m_dwDelayTime = 1000;   // Default to a delay time of 1000 ms.
    
    ```

    

Ensuite, déclarez deux nouvelles variables membres pour stocker le pourcentage de signal d’effet et le pourcentage de signal source à mélanger dans la mémoire tampon de sortie finale. Le terme « mouillé » fait référence à l’effet et le terme « secs » fait référence au signal source. Ajoutez les déclarations suivantes à ECHO. h :


```C++
double  m_fWetMix;    // percentage of effect
double  m_fDryMix;    // percentage of dry signal

```



Ces valeurs sont stockées sous forme de représentations décimales de pourcentages afin d’être facilement utilisées comme facteurs de mise à l’échelle. Par exemple, un mélange d’effets de 50% et de signal source de 50% serait représenté comme valeur de 0,50 pour chaque variable. La somme des valeurs pour m \_ fWetMix et m \_ fDryMix ne doit pas être supérieure à 1,0 (100 pour cent). Finalement, ces valeurs sont accessibles en tant que propriétés.

Ajoutez le code suivant au constructeur CEcho pour définir les valeurs par défaut à 50 pour cent chacune :


```C++
m_fWetMix = 0.50;  // default to 50 percent wet
m_fDryMix = 0.50;  // default to 50 percent dry

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exemples de propriétés Echo**](echo-sample-properties.md)
</dt> </dl>

 

 




