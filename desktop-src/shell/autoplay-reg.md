---
description: Il existe de nombreuses situations où l’exécution automatique peut être désactivée de manière temporaire ou permanente.
ms.assetid: 5e65a3d8-04b9-46ba-b4e5-a976e1923bfd
title: Activation et désactivation de l’exécution automatique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a567f50db75cd129346e193e66ba0ae5f74fa955
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393455"
---
# <a name="enabling-and-disabling-autorun"></a>Activation et désactivation de l’exécution automatique

Il existe de nombreuses situations où l’exécution automatique peut être désactivée de manière temporaire ou permanente. Par exemple, l’exécution automatique peut interférer avec le fonctionnement d’une application en cours d’exécution et doit être désactivée pendant toute la durée. Le système offre plusieurs moyens de désactiver l’exécution automatique.

-   [Suppression de l’exécution automatique par programmation](#suppressing-autorun-programmatically)
-   [Utilisation du Registre pour désactiver l’exécution automatique](#using-the-registry-to-disable-autorun)
-   [Exécution automatique pour d’autres types de supports de stockage](#autorun-for-other-types-of-storage-media)

## <a name="suppressing-autorun-programmatically"></a>Suppression de l’exécution automatique par programmation

Il existe plusieurs situations dans lesquelles l’exécution automatique peut être supprimée par programmation. En voici deux exemples:

-   Votre application dispose d’un programme d’installation qui oblige l’utilisateur à insérer un autre disque pouvant contenir un fichier autorun. inf.
-   Pendant le fonctionnement de votre application, l’utilisateur peut être amené à insérer un autre disque pouvant contenir un fichier autorun. inf.

Dans les deux cas, vous ne souhaitez généralement pas lancer une autre application tant que l’original est en cours.

Les utilisateurs peuvent supprimer manuellement l’exécution automatique en maintenant la touche Maj enfoncée lorsqu’ils insèrent le CD-ROM. Toutefois, il est généralement préférable de gérer cette opération par programme plutôt qu’en fonction de l’utilisateur.

Avec les systèmes qui disposent de Shell [version 4,70](versions.md) et versions ultérieures, Windows envoie un message « QueryCancelAutoPlay » à la fenêtre de premier plan. Votre application peut répondre à ce message pour supprimer l’exécution automatique. Cette approche est utilisée par les utilitaires système tels que la boîte de dialogue [ouvrir](../dlgbox/open-and-save-as-dialog-boxes.md) un courant pour désactiver l’exécution automatique.

Les fragments de code suivants montrent comment configurer et gérer ce message. Votre application doit être en cours d’exécution dans la fenêtre de premier plan. Tout d’abord, inscrivez « QueryCancelAutoPlay » en tant que message Windows :


```C++
uMessage = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
```



La fenêtre de votre application doit être au premier plan pour recevoir ce message. Le gestionnaire de messages doit retourner la **valeur true** pour annuler l’exécution automatique et **false** pour l’activer. Le fragment de code suivant illustre l’utilisation de ce message pour désactiver l’exécution automatique.


```C++
UINT g_uQueryCancelAutoPlay = 0;

LRESULT WndProc(HWND hwnd, UINT uMsg,  WPARAM wParam, LPARAM lParam) 
{ 
    switch (uMsg) 
    { 
    ... 
    default: 
        if (!g_uQueryCancelAutoPlay)
        { 
            g_uQueryCancelAutoPlay = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
        } 
        if (uMsg && uMsg == g_uQueryCancelAutoPlay)
        { 
            return TRUE;       // Cancel AutoRun
        }
    }
}
```



Si votre application utilise une boîte de dialogue et doit répondre à un message « QueryCancelAutoPlay », elle ne peut pas simplement retourner **true** ou **false**. Au lieu de cela, appelez [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) avec *NIndex* défini sur **DWL \_ MSGRESULT**. Affectez la valeur **true** au paramètre *dwNewLong* pour annuler l’exécution automatique, et **false** pour l’activer. Par exemple, l’exemple de procédure de boîte de dialogue suivant annule l’exécution automatique lorsqu’il reçoit un message « QueryCancelAutoPlay ».


```C++
UINT g_uQueryCancelAutoPlay = 0;

BOOL DialogProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    switch (uMsg) 
    { 
    ...
    default: 
        if (!g_uQueryCancelAutoPlay)
        {
            g_uQueryCancelAutoPlay = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
        } 
        if (uMsg == g_uQueryCancelAutoPlay) 
        {
            SetWindowLong(hDlg, DWL_MSGRESULT, TRUE);          
            return 1;               
        }
    } 
```



## <a name="using-the-registry-to-disable-autorun"></a>Utilisation du Registre pour désactiver l’exécution automatique

Il existe deux valeurs de Registre qui peuvent être utilisées pour désactiver de manière permanente l’exécution automatique : NoDriveAutoRun et NoDriveTypeAutoRun. La première valeur désactive l’exécution automatique pour les lettres de lecteur spécifiées et la seconde désactive l’exécution automatique pour une classe de lecteurs. Si l’une de ces valeurs est définie pour désactiver l’exécution automatique pour un appareil particulier, elle est désactivée. Consultez l’article de la base de connaissances [Comment désactiver la fonctionnalité d’exécution automatique dans Windows](https://support.microsoft.com/kb/967715) pour plus d’informations sur la désactivation de la fonctionnalité d’exécution automatique. Cet article répertorie les différentes mises à jour que vous devez avoir installées pour désactiver correctement la fonctionnalité d’exécution automatique.

> [!Note]  
> Les valeurs NoDriveAutoRun et NoDriveTypeAutoRun doivent uniquement être modifiées par les administrateurs système pour modifier la valeur de l’ensemble du système à des fins de test ou d’administration. Les applications ne doivent pas modifier ces valeurs, car il n’existe aucun moyen de les restaurer de manière fiable à leurs valeurs d’origine.

 

La valeur NoDriveAutoRun désactive l’exécution automatique pour les lettres de lecteur spécifiées. Il s’agit d’une valeur de données de Registre \_ DWORD, trouvée sous la clé suivante :

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

Le premier bit de la valeur correspond au lecteur A :, au deuxième à B :, et ainsi de suite. Pour désactiver l’exécution automatique pour une ou plusieurs lettres de lecteur, définissez les bits correspondants. Par exemple, pour désactiver les lecteurs A : et C :, affectez à NoDriveAutoRun la valeur `0x00000005` .

La valeur NoDriveTypeAutoRun désactive l’exécution automatique pour une classe de lecteurs. Il s’agit d’une \_ valeur de données binaires reg DWORD ou de 4 octets \_ , trouvée sous la même clé.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

En définissant les bits du premier octet de cette valeur, différents lecteurs peuvent être exclus de l’utilisation de l’exécution automatique.

Le tableau suivant indique les constantes bits et de masque de bits, qui peuvent être définies dans le premier octet de NoDriveTypeAutoRun pour désactiver l’exécution automatique pour un type de lecteur particulier. Vous devez redémarrer l’Explorateur Windows pour que les modifications soient prises en compte.



| Nombre de bits | Constante de masque binaire      | Description                                             |
|------------|-----------------------|---------------------------------------------------------|
| 0x04       | **LECTEUR à \_ Supprimer** | Un disque peut être supprimé d’un lecteur (par exemple une disquette). |
| 0x08       | **LECTEUR \_ fixe**      | Impossible de supprimer le disque du lecteur (disque dur).        |
| 0x10       | **LECTEUR \_ distant**     | Lecteur réseau.                                          |
| 0x20       | **LECTEUR \_ cdrom**      | Lecteur de CD-ROM                                           |
| 0x40       | **LECTEUR \_ ramdisk**    | Disque RAM.                                               |



 

## <a name="autorun-for-other-types-of-storage-media"></a>Exécution automatique pour d’autres types de supports de stockage

L’exécution automatique est principalement destinée à la distribution publique des applications sur CD-ROM et DVD-ROM, et son utilisation est déconseillée pour d’autres supports de stockage. Toutefois, il est souvent utile d’activer l’exécution automatique sur d’autres types de supports de stockage amovibles. Cette fonctionnalité est généralement utilisée pour simplifier le débogage des fichiers AutoRun. inf. L’exécution automatique fonctionne uniquement sur les périphériques de stockage amovibles lorsque les critères suivants sont satisfaits :

-   L’appareil doit avoir des pilotes compatibles avec l’exécution automatique. Pour être compatible avec l’exécution automatique, un pilote doit informer le système qu’un disque a été inséré en envoyant un message [**WM \_ DEVICECHANGE**](../devio/wm-devicechange.md) .
-   Le répertoire racine du support inséré doit contenir un fichier autorun. inf.
-   L’exécution de l’exécution automatique ne doit pas être désactivée dans le [Registre](#using-the-registry-to-disable-autorun).
-   L’application de premier plan n’a pas [supprimé](#suppressing-autorun-programmatically) l’exécution automatique.

> [!Note]  
> Cette fonctionnalité ne doit pas être utilisée pour distribuer des applications sur un support amovible. Étant donné que l’implémentation de l’exécution automatique sur un support amovible offre un moyen simple de propager des virus informatiques, les utilisateurs doivent être suspects de toute disquette distribuée publiquement qui contient un fichier autorun. inf.

 

Normalement, l’exécution automatique démarre automatiquement, mais elle peut également être démarrée manuellement. Si l’appareil est conforme aux critères ci-dessus, le menu contextuel de la lettre de lecteur inclut une commande d' **exécution automatique** . Pour exécuter l’exécution automatique manuellement, cliquez avec le bouton droit sur l’icône du lecteur et sélectionnez **exécution automatique** dans le menu contextuel ou double-cliquez sur l’icône du lecteur. Si les pilotes ne sont pas compatibles avec l’exécution automatique, le menu contextuel n’a pas d’élément de **lecture automatique** et l’exécution automatique ne peut pas être démarrée.

Les pilotes compatibles avec l’exécution automatique sont fournis avec des lecteurs de disque amovibles, ainsi que d’autres types de supports amovibles, tels que les cartes CompactFlash. AutoRun fonctionne également avec les lecteurs réseau mappés à une lettre de lecteur avec l’Explorateur Windows ou montés avec la [console MMC (Microsoft Management Console)](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page). Comme pour le matériel monté, un lecteur réseau monté doit avoir un fichier autorun. inf dans son répertoire racine et ne doit pas être désactivé par le biais du [Registre](#using-the-registry-to-disable-autorun).

 

 
