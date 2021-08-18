---
description: Les utilisateurs peuvent configurer le débogage automatique pour les aider à déterminer la raison pour laquelle leur système ou une application a cessé de répondre.
ms.assetid: c3c7aa98-c298-452c-b8d0-10a08b4d82a3
title: Configuration du débogage automatique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990f2f52e6227e4b1a2cf92656794c90fb5d465915a5d888025d0f3b2c438630
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076503"
---
# <a name="configuring-automatic-debugging"></a>Configuration du débogage automatique

Les utilisateurs peuvent configurer le débogage automatique pour les aider à déterminer la raison pour laquelle leur système ou une application a cessé de répondre.

## <a name="configuring-automatic-debugging-for-system-crashes"></a>Configuration du débogage automatique pour les pannes système

Pour configurer l’ordinateur cible afin de générer un fichier de vidage sur incident lorsque le système ne répond plus, utilisez l’application **système** dans le panneau de configuration. Cliquez sur **paramètres système avancés**, qui affiche la boîte de dialogue **Propriétés système** . sous l’onglet **avancé** de cette zone, cliquez sur **Paramètres** sous **démarrage et récupération**, puis utilisez les options de récupération appropriées. Vous pouvez également configurer les options de vidage sur incident à l’aide de la clé de Registre suivante :

**HKEY \_ \_** \\  \\  \\ **Contrôle** CurrentControlSet du système \\  de l’ordinateur local CrashControl

Le fichier que vous pouvez spécifier est le fichier de vidage sur incident. Son nom par défaut est Memory. dmp. Vous pouvez déboguer un vidage sur incident à l’aide d’un débogueur en mode noyau, tel que WinDbg ou KD. Pour plus d’informations, consultez la documentation fournie avec le débogueur.

## <a name="configuring-automatic-debugging-for-application-crashes"></a>Configuration du débogage automatique pour les incidents d’application

Lorsqu’une application cesse de répondre (par exemple, après une violation d’accès), le système appelle automatiquement un débogueur qui est spécifié dans le registre pour le débogage post-mortem, l’ID de processus et le descripteur d’événement sont passés au débogueur si la ligne de commande est correctement configurée. La procédure suivante décrit comment spécifier un débogueur dans le registre.

**Pour définir un débogueur en tant que débogueur post-mortem**

1.  Accédez à la clé de Registre suivante :

    **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AeDebug**

2.  Ajoutez ou modifiez la valeur du **débogueur** à l’aide d’une chaîne de Registre \_ SZ qui spécifie la ligne de commande pour le débogueur.

    La chaîne doit inclure le chemin d’accès complet au fichier exécutable du débogueur. Indiquez l’ID de processus et le descripteur d’événement avec les paramètres « % LD » dans la ligne de commande du débogueur. Différents débogueurs peuvent avoir leurs propres syntaxes de paramètre pour indiquer ces valeurs. Quand le débogueur est appelé, le premier « % LD » est remplacé par l’ID de processus et le deuxième « % LD » est remplacé par le handle d’événement.

    Le texte suivant est un exemple de configuration de WinDbg en tant que débogueur.

    ``` syntax
    "C:\debuggers\windbg.exe" -p %ld -e %ld -g
    ```

3.  Si vous souhaitez que le débogueur soit appelé sans intervention de l’utilisateur, ajoutez ou modifiez la valeur **auto** , à l’aide d’une \_ chaîne sz reg qui spécifie si le système doit afficher une boîte de dialogue à l’utilisateur avant que le débogueur ne soit appelé. La chaîne « 1 » désactive la boîte de dialogue. la chaîne « 0 » active la boîte de dialogue.

## <a name="excluding-an-application-from-automatic-debugging"></a>Exclusion d’une application du débogage automatique

La procédure suivante décrit comment exclure une application du débogage automatique une fois que la valeur **auto** sous la clé **AeDebug** a été définie sur 1.

**Pour exclure une application du débogage automatique**

1.  Accédez à la clé de Registre suivante :

    **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AeDebug**

2.  Ajoutez une \_ valeur reg DWORD à la sous-clé **AutoExclusionList** , où le nom est le nom du fichier exécutable et la valeur est 1. Par défaut, le Gestionnaire de fenêtrage (Dwm.exe) est exclu du débogage automatique, sinon un blocage du système peut se produire si Dwm.exe cesse de répondre (l’utilisateur ne peut pas voir l’interface affichée par le débogueur, car Dwm.exe ne répond pas, et Dwm.exe ne peut pas se terminer parce qu’il est détenu par le débogueur).

    **Windows Server 2003 et Windows XP :** La sous-clé **AutoExclusionList** n’est pas disponible. vous ne pouvez donc pas exclure une application, y compris Dwm.exe, du débogage automatique.

Les entrées de Registre **AeDebug** par défaut peuvent être représentées comme suit :

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows NT
            CurrentVersion
               AeDebug
                  Auto = 1
                  AutoExclusionList
                     DWM.exe = 1
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Activation du débogage post-mortem avec WinDbg](/windows-hardware/drivers/debugger/enabling-postmortem-debugging)
</dt> </dl>

 

 
