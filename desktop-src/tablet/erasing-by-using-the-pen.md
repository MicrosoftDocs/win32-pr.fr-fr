---
description: Si vous choisissez d’implémenter l’effacement dans votre application à l’aide de l’objet InkOverlay, vous pouvez le faire à l’aide de l’une des deux méthodes suivantes.
ms.assetid: c05c7dbf-c3e0-42a7-a97e-bb9d9764209d
title: Effacement à l’aide du stylet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9e71828e826f2d57dd21e57934e12c8de0be03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393520"
---
# <a name="erasing-by-using-the-pen"></a>Effacement à l’aide du stylet

Si vous choisissez d’implémenter l’effacement dans votre application à l’aide de l’objet [**InkOverlay**](inkoverlay-class.md) , vous pouvez le faire à l’aide de l’une des deux méthodes suivantes.

## <a name="using-the-tip-of-the-pen"></a>Utilisation de l’info-bulle du stylet

La pointe du stylet est généralement utilisée pour l’écriture manuscrite et le dessin. Toutefois, le Conseil peut également être utilisé pour effacer l’encre. Pour ce faire, l’application doit disposer d’un mode d’effacement que les utilisateurs peuvent employer. Dans ce mode, utilisez le test de positionnement pour déterminer l’encre sur laquelle le curseur est déplacé. Vous pouvez définir le mode d’effacement pour supprimer uniquement l’encre sur laquelle le curseur passe ou les traits entiers qui croisent le chemin d’accès du curseur, en fonction de la conception ou des considérations fonctionnelles.

Pour obtenir un exemple d’utilisation d’un mode d’effacement pour effacer l’encre, consultez l’exemple d’effacement d' [encre](ink-erasing-sample.md).

## <a name="using-the-top-of-the-pen"></a>En utilisant le haut du stylet

Pour implémenter l’effacement avec le haut du stylet du Tablet PC, votre application doit rechercher une modification dans le curseur. Pour rechercher le curseur inversé, écoutez l’événement [**CursorInRange**](inkoverlay-cursorinrange.md) pour déterminer quand le curseur se trouve dans le contexte de votre application. Lorsque le curseur se trouve dans la plage, recherchez la propriété [**inversée**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) sur l’objet [**curseur**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) . Si la propriété **inversée** a la **valeur true**, effectuez un test de positionnement pour déterminer l’encre sur laquelle le curseur est déplacé. Effacez l’encre ou les traits qui croisent le chemin d’accès du curseur, en fonction de la conception ou des considérations fonctionnelles.

Pour obtenir un exemple d’utilisation du haut du stylet pour effacer l’encre, consultez l' [exemple d’effacement d’encre](ink-erasing-sample.md).

### <a name="determining-if-erasing-with-the-top-of-the-pen-is-enabled"></a>Détermination de l’activation de l’effacement avec le haut du stylet

Les utilisateurs peuvent utiliser le haut du stylet pour effacer l’encre dans les applications conçues pour Tablet PC, si leur matériel spécifique le permet. Cette fonctionnalité est accessible par une case à cocher dans la zone de groupe boutons du stylet sous l’onglet Options du stylet de la boîte de dialogue Paramètres du Tablet PC et du stylet. Pour déterminer si l’utilisateur a activé l’effacement pour le haut du stylet, vérifiez la sous-clé de Registre suivante :

`HKEY_CURRENT_USER\SOFTWARE\Microsoft\WISP\PEN\SysEventParameters`

L' `EraseEnable` entrée de cette sous-clé est de type **reg \_ DWORD**. La valeur de cette entrée est 1 pour activé, ou 0 pour désactivé. Les autres valeurs sont réservées pour un usage ultérieur.

Si votre application autorise l’utilisation du haut du stylet pour l’effacement, vous devez vérifier et mettre en cache la valeur de l’entrée EraseEnable dans les cas suivants :

-   Votre application démarre.
-   Chaque fois que votre application reçoit le focus après avoir perdu le focus.

Utilisez cette valeur mise en cache pour modifier le comportement de votre application de manière appropriée.

L’exemple C suivant \# définit une `GetEraseEnabled` méthode qui vérifie la valeur de l' `EraseEnable` entrée de la `SysEventParameters` sous-clé. La `GetEraseEnabled` méthode retourne **true** si la valeur de l’entrée est 1 ; retourne **false** si la valeur de l’entrée est 0, ou lève une [exception InvalidOperationException](/dotnet/api/system.invalidoperationexception) si la valeur de l’entrée est différente de 1 ou 0. La `GetEraseEnabled` méthode retourne la valeur attendue **true** si la sous-clé ou l’entrée n’est pas présente.


```C++
private bool GetEraseEnabled()
{
    // 0 is disabled, 1 is enabled. The default is enabled
    const int Enabled = 1;
    const int Disabled = 0;
    const int DefaultValue = Enabled;

    // Constants for the registry subkey and the entry
    const string Subkey =
                @"SOFTWARE\Microsoft\WISP\PEN\SysEventParameters";
    const string KeyEntry = "EraseEnable";

    // Open the registry subkey.
    Microsoft.Win32.RegistryKey regKey =
        Microsoft.Win32.Registry.CurrentUser.OpenSubKey(Subkey);

    // Retrieve the value of the EraseEnable subkey entry. If either
    // the subkey or the entry does not exist, use the default value.
    object keyValue = (null == regKey) ? DefaultValue :
        regKey.GetValue(KeyEntry,DefaultValue);

    switch((int)keyValue)
    {
        case Enabled:
            // Return true if erasing on pen inversion is enabled. 
            return true;
        case Disabled:
            // Return false if erasing on pen inversion is disabled. 
            return false;
        default:
            // Otherwise, throw an exception. Do not assume this is
            // a Boolean value. Enabled and Disabled are the values
            // defined for this entry at this time. Other values are
            // reserved for future use.
            throw new InvalidOperationException(
                "Unexpected registry subkey value.");
    }
}
```



 

 
