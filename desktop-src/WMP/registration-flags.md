---
title: Indicateurs d’inscription
description: Indicateurs d’inscription
ms.assetid: ba1709c2-0fe5-4168-9aed-613d01eff21f
keywords:
- plug-ins Lecteur Windows Media, indicateurs d’inscription
- plug-ins, indicateurs d’inscription
- plug-ins d’interface utilisateur, indicateurs d’inscription
- Plug-ins d’interface utilisateur, indicateurs d’inscription
- indicateurs, plug-ins d’interface utilisateur
- Registre, plug-ins d’interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbd34ed98236f8a02c936d52b092b82be60b986fb7b16edce1f3b1cbb91d6a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002809"
---
# <a name="registration-flags"></a>Indicateurs d’inscription

lorsque l’assistant de plug-in Lecteur Windows Media crée un projet de plug-in d’interface utilisateur, il crée une clé dans le registre qui contient des informations sur le plug-in. Cette clé est créée à l’emplacement suivant :


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\UIPlugins\{ClassId}
```



*ClassID* est l’ID de classe du plug-in.

Cette clé comprend les valeurs suivantes.



| Nom                     | Type       | Description                                                                                                                                                                               |
|--------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fonctionnalités             | \_valeur DWORD reg | Valeur DWORD qui se compose d’au moins un indicateur de type de plug-in qui peut être combiné avec un ou plusieurs indicateurs de fonctionnalités de plug-in à l’aide de binaires ou d’opérations.                             |
| Description              | SZ de REG \_    | Chaîne qui contient la description du plug-in. L’Assistant de plug-in crée une ressource de type chaîne et fournit l’URL de la ressource (à l’aide du protocole res) pour cette valeur.         |
| FriendlyName             | SZ de REG \_    | Chaîne qui contient le nom lisible par l’utilisateur pour le plug-in. L’Assistant de plug-in crée une ressource de type chaîne et fournit l’URL de la ressource (à l’aide du protocole res) pour cette valeur. |
| UninstallPath (facultatif) | SZ de REG \_    | Chaîne qui contient le chemin d’accès à un fichier exécutable qui désinstalle le plug-in.                                                                                                        |



 

Pour plus d’informations sur le protocole res, consultez le kit de développement logiciel (SDK) Internet Development.

Le tableau suivant détaille les indicateurs de type de plug-in.



| Indicateur de type de plug-in                | Valeur | Description                                       |
|----------------------------------|-------|---------------------------------------------------|
| **\_arrière-plan du type de plug \_ -in**     | 0x1   | Le plug-in d’interface utilisateur n’affiche pas d’interface utilisateur. |
| **TYPE de plug-in \_ \_ SEPARATEWINDOW** | 0x2   | Le plug-in d’interface utilisateur est un plug-in de fenêtre distinct.      |
| **TYPE de plug-in \_ \_ DISPLAYAREA**    | 0x3   | Le plug-in d’interface utilisateur est un plug-in de zone d’affichage.         |
| **TYPE de plug-in \_ \_ SETTINGSAREA**   | 0x4   | Le plug-in d’interface utilisateur est un plug-in de zone de paramètres.        |
| **TYPE de plug-in \_ \_ METADATAAREA**   | 0x5   | Le plug-in d’interface utilisateur est un plug-in de zone de métadonnées.        |



 

Le tableau suivant détaille les indicateurs de fonctionnalités de plug-in.



| Indicateur de fonctionnalités de plug-in             | Valeur      | Description                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **indicateurs de plug-in \_ \_ ACCEPTSMEDIA**       | 0x10000000 | le plug-in d’interface utilisateur peut accepter des tableaux de pointeurs d’objets **multimédias** quand Lecteur Windows Media appelle [**IWMPPluginUI :: SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .                                                                                                                                                                                                                                                           |
| **indicateurs de plug-in \_ \_ ACCEPTSPLAYLISTS**   | 0x8000000  | le plug-in d’interface utilisateur peut accepter des tableaux de pointeurs d’objets **Playlist** quand Lecteur Windows Media appelle [**IWMPPluginUI :: SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .                                                                                                                                                                                                                                                        |
| **indicateurs de plug-in \_ \_ HASPRESETS**         | 0x4000000  | Le plug-in d’interface utilisateur utilise des présélections. si le plug-in spécifie cet indicateur, Lecteur Windows Media interroge le plug-in pour obtenir des informations prédéfinies en appelant [**IWMPPluginUI :: GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty) .                                                                                                                                                                                                      |
| **indicateurs de plug-in \_ \_ HASPROPERTYPAGE**    | 0x80000000 | Le plug-in d’interface utilisateur fournit une boîte de dialogue de page de propriétés. Lecteur Windows Media appellera [**IWMPPluginUI ::D isplaypropertypage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) si cet indicateur est défini lors de l’appel de la page de propriétés.                                                                                                                                                                                                 |
| **indicateurs de plug-in \_ \_ masqués**             | 0x02000000 | Le plug-in IU d’arrière-plan n’apparaît pas dans le menu **plug-ins** accessible à partir des menus **affichage** ou **Outils** ou du bouton **Sélectionner les options de diffusion** en cours. Il apparaît dans l’onglet **plug-ins** de la boîte de dialogue Options. L’icône d’exécution du plug-in en arrière-plan s’affiche alors dans la barre d’État. Cet indicateur n’a aucun effet sur les plug-ins autres que les plug-ins d’IU d’arrière-plan.<br/> |
| **indicateurs de plug-in \_ \_ INSTALLAUTORUN**     | 0x40000000 | Lecteur Windows Media exécute automatiquement le plug-in d’interface utilisateur lors de l’installation du plug-in.                                                                                                                                                                                                                                                                                                                               |
| **indicateurs de plug-in \_ \_ LAUNCHPROPERTYPAGE** | 0x20000000 | Lecteur Windows Media appelle [**IWMPPluginUI ::D isplaypropertypage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) lorsque le plug-in d’interface utilisateur s’exécute pour la première fois. Si cet indicateur est spécifié, les **indicateurs de plug-in \_ \_ HASPROPERTYPAGE** doivent également être spécifiés.<br/>                                                                                                                                                             |



 

Les constantes suivantes sont définies dans wmpplug. h. Ne modifiez pas les valeurs associées à ces constantes.



| Nom                                    | Description                               |
|-----------------------------------------|-------------------------------------------|
| **PLUG-in \_ INSTALLREGKEY**               | Emplacement de la clé de registre de plug-in. |
| **PLUG-in \_ INSTALLREGKEY \_ FRIENDLYNAME** | Nom de la valeur de nom convivial.      |
| **Description du plug-in \_ INSTALLREGKEY \_**  | Nom de la valeur de description.        |
| **\_fonctionnalités INSTALLREGKEY du plug-in \_** | Nom de la valeur des fonctionnalités.       |
| **désinstaller le plug-in \_ INSTALLREGKEY \_**    | Nom de la valeur du chemin d’accès de désinstallation.     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IWMPPluginUI ::D isplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage)
</dt> <dt>

[**IWMPPluginUI :: GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty)
</dt> <dt>

[**IWMPPluginUI :: SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty)
</dt> <dt>

[**Informations de référence sur la programmation de plug-ins d’interface utilisateur**](user-interface-plug-ins-programming-reference.md)
</dt> </dl>

 

 





