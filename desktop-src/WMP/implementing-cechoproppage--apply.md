---
title: Implémentation de CEchoPropPage Apply
description: Implémentation de CEchoPropPage Apply
ms.assetid: e887b851-e623-4ec4-8d8b-165e4b21e116
keywords:
- Plug-ins du lecteur Windows Media, pages de propriétés de l’exemple Echo
- plug-ins, pages de propriétés d’exemple Echo
- plug-ins de traitement de signal numérique, pages de propriétés d’exemple Echo
- Plug-ins DSP, pages de propriétés d’exemple Echo
- Exemple de plug-in DSP Echo, pages de propriétés
- Echo DSP, exemple de plug-in, méthode Apply CEchoPropPage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bdca8a771d3e3e26923567f25bf7d19e968595e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840198"
---
# <a name="implementing-cechoproppageapply"></a>Implémentation de CEchoPropPage :: apply

La méthode CEchoPropPage :: apply est implémentée dans EchoPropPage. cpp. Elle s’exécute lorsque l’utilisateur clique sur **appliquer** dans la boîte de dialogue page de propriétés du lecteur Windows Media. L’exemple de code de l’Assistant de plug-in fournit une implémentation pour gérer une seule propriété. Vous pouvez modifier ce code pour l’un des exemples de propriétés Echo, puis ajouter du code pour stocker l’autre valeur de propriété.

## <a name="declaring-the-apply-method-variables"></a>Déclaration des variables de méthode Apply

Tout d’abord, vous devez supprimer la déclaration de fScaleFactor. Ensuite, ajoutez les déclarations de variables dont vous aurez besoin. L’exemple suivant montre les déclarations de variables terminées :


```
TCHAR   szStr[MAXSTRING] = { 0 };
DWORD   dwDelayTime = 1000;  // Initialize the delay time.
DWORD   dwWetmix = 50;       // Initialize a DWORD for effect level.
double  fWetmix = 0.50;      // Initialize a double for effect level.
```



## <a name="retrieving-the-values-from-the-property-page"></a>Récupération des valeurs à partir de la page de propriétés

Vous devez implémenter le code pour récupérer et valider les entrées utilisateur. L’exemple de code suivant récupère la valeur de temps de délai dans la \_ zone d’édition IDC DELAYTIME, puis vérifie que la valeur est comprise dans une plage spécifiée :


```
// Get the delay time value from the dialog box.
GetDlgItemText(IDC_DELAYTIME, szStr, sizeof(szStr) / sizeof(szStr[0]));

dwDelayTime = atoi(szStr);

// Make sure delay time is valid.
if ((dwDelayTime < 10) || (dwDelayTime > 2000))
{
    if (::LoadString(_Module.GetResourceInstance(), IDS_DELAYRANGEERROR, szStr, sizeof(szStr) / sizeof(szStr[0])))
    {
        MessageBox(szStr);
    }

    return E_FAIL;
}
```



Si l’entrée utilisateur n’est pas dans la plage spécifiée, le code affiche une boîte de message. Notez l’utilisation de la ressource de type chaîne que vous avez créée précédemment pour le message d’erreur.

L’exemple suivant récupère le niveau d’effet à partir de la \_ zone d’édition IDC WETMIX, puis vérifie que la valeur est comprise dans une plage spécifiée :


```
// Get the effects level value from the dialog box.
GetDlgItemText(IDC_WETMIX, szStr, sizeof(szStr) / sizeof(szStr[0]));

dwWetmix = atoi(szStr);

// Make sure wet mix value is valid.
if ((dwWetmix < 0) || (dwWetmix > 100))
{
    if (::LoadString(_Module.GetResourceInstance(), IDS_MIXRANGEERROR, szStr, sizeof(szStr) / sizeof(szStr[0])))
    {
        MessageBox(szStr);
    }

    return E_FAIL;
}
```



## <a name="storing-the-property-values-in-the-registry"></a>Stockage des valeurs de propriété dans le registre

Ensuite, votre code doit conserver les nouvelles valeurs de propriété dans le registre. Le code suivant stocke les deux valeurs de propriété :


```
// update the registry
CRegKey key;
LONG    lResult;

// Write the delay time value to the registry.
lResult = key.Create(HKEY_CURRENT_USER, kszPrefsRegKey);
if (ERROR_SUCCESS == lResult)
{
    lResult = key.SetValue( dwDelayTime , kszPrefsDelayTime );
}

// Write the wet mix value to the registry.
lResult = key.Create(HKEY_CURRENT_USER, kszPrefsRegKey);
if (ERROR_SUCCESS == lResult)
{
    lResult = key.SetValue( dwWetmix , kszPrefsWetmix );
}
```



## <a name="updating-the-echo-plug-in-property-values"></a>Mise à jour des valeurs de propriété du plug-in Echo

La méthode **apply** doit informer le plug-in ECHO que les valeurs des propriétés ont changé. Le code suivant appelle la méthode put de propriété pour chaque propriété à l’aide du pointeur d’interface récupéré dans CEchoPropPage :: SetObjects :


```
// update the plug-in
if (m_spEcho)
{
    m_spEcho->put_delay(dwDelayTime);

    // Convert the wet mix value from DWORD to double.
    fWetmix = (double)dwWetmix / 100;
    m_spEcho->put_wetmix(fWetmix);
}
```



Notez que la valeur de la combinaison humide est convertie en virgule flottante avant d’être transmise au plug-in.

## <a name="disabling-the-apply-button"></a>Désactivation du bouton appliquer

En guise de dernière étape, votre code doit désactiver l’application dans la boîte de dialogue page de propriétés en tant que signal à l’utilisateur que les valeurs ont été correctement mises à jour. Pour cela, vous devez disposer de la seule ligne de code suivante :


```
m_bDirty = FALSE; // Tell the property page to disable Apply.
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Modification de la page de propriétés de l’exemple Echo**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




