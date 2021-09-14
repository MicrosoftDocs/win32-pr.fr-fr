---
title: Implémentation de CEchoPropPage OnInitDialog
description: Implémentation de CEchoPropPage OnInitDialog
ms.assetid: 568989b0-bc07-480f-8b5c-41bbada713f8
keywords:
- plug-ins Lecteur Windows Media, pages de propriétés de l’exemple Echo
- plug-ins, pages de propriétés d’exemple Echo
- plug-ins de traitement de signal numérique, pages de propriétés d’exemple Echo
- Plug-ins DSP, pages de propriétés d’exemple Echo
- Exemple de plug-in DSP Echo, pages de propriétés
- Echo DSP, exemple de plug-in, CEchoPropPage OnInitDialog, méthode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0874c750914b5caecf86ffa61a0c42d38bb1c02e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008426"
---
# <a name="implementing-cechoproppageoninitdialog"></a>Implémentation de CEchoPropPage :: OnInitDialog

La méthode **CEchoPropPage :: OnInitDialog** est implémentée dans EchoPropPage. cpp. Elle s’exécute lorsque la boîte de dialogue page de propriétés est appelée. Le code de cette méthode doit récupérer les valeurs de propriété actuelles et les afficher dans la zone d’édition appropriée. L’exemple de code de l’Assistant de plug-in fournit une implémentation pour une propriété unique. Vous pouvez modifier ce code pour l’un des exemples de propriétés Echo, puis ajouter du code pour récupérer la deuxième valeur de propriété.

## <a name="declaring-the-oninitdialog-method-variables"></a>Déclaration des variables de méthode OnInitDialog

Tout d’abord, vous devez supprimer la déclaration de fScaleFactor et la remplacer par les déclarations de variables suivantes :


```
DWORD  dwDelayTime = 1000;    // Default delay time.
DWORD  dwWetmix = 50;         // Default wet mix DWORD.
double fWetmix =  0.50;       // Default wet mix double.
```



## <a name="retrieving-the-current-values-from-the-plug-in"></a>Récupération des valeurs actuelles du plug-in

Le code doit ensuite tenter de récupérer les valeurs de propriété actuelles à partir du plug-in Echo. L’exemple suivant tente de récupérer chaque propriété :


```
if (m_spEcho)
{
    m_spEcho->get_delay(&dwDelayTime);
    m_spEcho->get_wetmix(&fWetmix);
    // Convert wet mix from double to DWORD.
    dwWetmix = (DWORD)(fWetmix * 100);
}
```



La boîte de dialogue affiche la valeur de niveau d’effet pour l’utilisateur sous la forme d’un entier, mais le plug-in stocke la valeur sous la forme d’un nombre à virgule flottante. Par conséquent, le code convertit la valeur à virgule flottante en valeur **DWORD** .

## <a name="retrieving-the-current-values-from-the-registry"></a>Récupération des valeurs actuelles à partir du Registre

Si la page de propriétés ne peut pas récupérer les valeurs actuelles du plug-in, elle doit tenter de les lire à partir du Registre. Le code suivant lit chaque valeur de propriété :


```
else // Otherwise, read values from registry
{
    CRegKey key;
    LONG    lResult;

    lResult = key.Open(HKEY_CURRENT_USER, kszPrefsRegKey, KEY_READ);
    if (ERROR_SUCCESS == lResult)
    {
        DWORD   dwValue = 0;

        // Read the delay time.
        lResult = key.QueryValue(dwValue, kszPrefsDelayTime );
        if (ERROR_SUCCESS == lResult)
        {
            dwDelayTime = dwValue;
        }

        // Read the wet mix value.
        lResult = key.QueryValue(dwValue, kszPrefsWetmix );
        if (ERROR_SUCCESS == lResult)
        {
            dwWetmix = dwValue;
        }
    }
}
```



Notez l’utilisation des constantes de registre que vous avez créées précédemment.

## <a name="displaying-the-values-to-the-user"></a>Affichage des valeurs pour l’utilisateur

Enfin, la page de propriétés doit afficher les valeurs dans les contrôles de zone d’édition appropriés. L’exemple de code suivant illustre ceci :


```
 TCHAR   szStr[MAXSTRING];

// Display the delay time.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwDelayTime);
SetDlgItemText(IDC_DELAYTIME, szStr);

// Display the effect level.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwWetmix);
SetDlgItemText(IDC_WETMIX, szStr);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Modification de la page de propriétés de l’exemple Echo**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




