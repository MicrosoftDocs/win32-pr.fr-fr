---
title: Gestion des événements d’acquisition de licence
description: Gestion des événements d’acquisition de licence
ms.assetid: e118bf09-1fa6-41b6-a6bb-3e8cb6097994
keywords:
- Windows Media Format SDK, gestion des événements d’acquisition de licence
- Windows Media Format SDK, événements d’acquisition de licence
- ASF (Advanced Systems Format), gestion des événements d’acquisition de licence
- ASF (format de systèmes avancés), gestion des événements d’acquisition de licence
- ASF (Advanced Systems Format), événements d’acquisition de licence
- ASF (format de systèmes avancés), événements d’acquisition de licence
- gestion des droits numériques (DRM), gestion des événements d’acquisition de licence
- DRM (gestion des droits numériques), gestion des événements d’acquisition de licence
- gestion des droits numériques (DRM), événements d’acquisition de licence
- DRM (gestion des droits numériques), événements d’acquisition de licence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e31fd5b108f41d5b0925918fdf1c83764bcf7e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295175"
---
# <a name="handling-license-acquisition-events"></a>Gestion des événements d’acquisition de licence

Une application de lecteur compatible DRM, dans sa méthode de rappel [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) , gère les quatre événements suivants liés au processus d’acquisition de licence :

-   **État de la \_ signature LICENSEURL WMT \_ \_**
-   **WMT \_ aucun \_ droit**
-   **WMT \_ aucun \_ droit \_ ex**
-   **\_licence d’acquisition WMT \_**

**État de la \_ signature LICENSEURL WMT \_ \_**

Lorsque le composant DRM détecte un contenu protégé par la version 7 de DRM, il recherche d’abord une licence valide sur le système local. S’il n’en existe aucun, il évalue l’URL d’acquisition de licence dans l’en-tête DRM du fichier et envoie un  événement d' **\_ \_ \_ État de signature LICENSEURL WMT** avec pValue défini sur l’une des valeurs d’approbation de l' [**\_ DRMLA \_ WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust) , indiquant si l’URL est approuvée, non approuvée ou a été falsifiée. Si l’URL n’est pas approuvée, l’application doit avertir l’utilisateur. Si l’URL a été falsifiée, le fichier doit être considéré comme endommagé, et l’application ne doit pas accéder à l’URL sans émettre de message d’avertissement fort à l’utilisateur.

**WMT \_ aucun \_ droit**

L’événement **WMT \_ no \_ Rights** n’est envoyé que pour le contenu DRM version 1, ce qui signifie que la licence doit être acquise non silencieusement. En d’autres termes, l’utilisateur doit accéder à une page Web pour obtenir une licence. L’URL de la page est récupérée sous la forme d’une chaîne à caractères larges se terminant par un caractère null à partir du paramètre *pValue* dans la méthode **OnStatus** .

Le cas échéant, une application peut permettre à l’utilisateur de naviguer plus facilement vers la page Web, soit en ouvrant Internet Explorer dans un processus distinct, soit en hébergeant le contrôle de navigateur Web. Toutefois, cela n’est pas obligatoire. Au minimum, une application peut simplement afficher l’URL de l’utilisateur dans une boîte de message et l’inviter à la coller dans la barre d’adresses d’Internet Explorer. L’exemple audioplayer illustre la gestion appropriée de l’événement de **\_ non- \_ autorisation WMT** , notamment la mise en forme de la chaîne d’URL et l’utilisation de la méthode **CreateProcess** pour ouvrir Internet Explorer et accéder à l’URL spécifiée.

Étant donné que l’application n’a aucun moyen de savoir quand une licence DRM version 1 a été acquise, il revient à l’utilisateur d’essayer d’ouvrir à nouveau le fichier après avoir acquis la licence.

Ce même processus d’acquisition de licence non silencieuse peut également être utilisé pour les licences de la version 7, mais dans ce cas, l’application peut commencer par appeler [**IWMDRMReader :: MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition). Cette méthode permet de vérifier la Banque de licences locale de manière répétée jusqu’à ce que la licence du nouveau fichier soit trouvée. À ce stade, l’application recevra un événement d' **\_ acquisition de \_ licence WMT** . Pour toutes les licences de la version 7, il est recommandé que les applications offrent aux utilisateurs la possibilité d’obtenir des licences en mode silencieux ou non en mode silencieux.

**WMT \_ aucun \_ droit \_ ex**

L’événement **WMT \_ no \_ Rights \_** (par exemple) indique que le contenu est protégé par DRM version 7. par conséquent, le processus d’acquisition de licence peut être exécuté en mode silencieux ou non en mode silencieux. En général, l’acquisition de licence silencieuse est plus pratique pour les utilisateurs finaux, bien que certaines personnes préfèrent acquérir toutes les licences de manière non silencieuse. Lorsque l’acquisition de licence oblige l’utilisateur à soumettre des informations personnelles ou de paiement, le processus doit toujours être effectué de manière non silencieuse. L’acquisition de licence non silencieuse est décrite ci-dessus sous l’en-tête de **\_ non- \_ autorisation WMT** . L’acquisition en mode silencieux se déroule comme suit :

1.  Effectuez un cast du paramètre *pValue* en une structure de [**\_ \_ \_ données de licence WM**](wm-get-license-data.md) et stockez la structure au cas où elle serait nécessaire ultérieurement pour une acquisition de licence non silencieuse.
2.  Appelez **QueryInterface** sur l’objet lecteur pour obtenir l’interface [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) .
3.  Appelez [**IWMDRMReader :: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) et spécifiez 0x1 dans le paramètre *dwFlags* pour indiquer l’acquisition en mode silencieux. Il s’agit d’un appel asynchrone qui est retourné immédiatement.
4.  Attendez l’événement **d' \_ acquisition de \_ licence WMT** .

**\_licence d’acquisition WMT \_**

L’événement d’acquisition de **\_ \_ licence WMT** est envoyé une fois que le processus d’acquisition de licence est terminé pour une licence DRM version 7. [**IWMDRMReader :: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) entraîne l’envoi de cet événement pour l’acquisition en mode silencieux, et [**MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition) provoque son envoi pour une acquisition non silencieuse. Dans votre gestionnaire d’événements, castez *pValue* en pointeur vers une structure de [**\_ \_ \_ données de licence WM**](wm-get-license-data.md) et examinez le membre **HR** pour déterminer si la licence a été acquise avec succès. Si **HR** est égal \_ à NS E \_ DRM \_ no \_ Rights, cela signifie que la licence doit être acquise non silencieusement. Les applications doivent permettre aux utilisateurs d’annuler le processus d’acquisition de licence à tout moment. Pour ce faire, appelez [**IWMDRMReader :: CancelLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancellicenseacquisition). L’appel de cette méthode enverra un événement d' **\_ acquisition de \_ licence WMT** avec une valeur **HRESULT** de NS \_ S \_ DRM \_ Acquire \_ Cancelled.

Si **HR** est égal à \_ \_ la licence DRM de NS S \_ \_ acquise, la licence a été acquise et l’application peut tenter de lire le fichier, ou la copier sur un périphérique ou exécuter l’action pour laquelle il a demandé des droits.

sur Windows XP, un nouveau code d’erreur a été introduit \_ : \_ NOTACQUIRED de licence DRM E \_ \_ . ce code d’erreur est généré chaque fois que les composants Windows Media Format runtime sur Windows XP ne parviennent pas à acquérir une licence lors de l’acquisition d’une licence en mode silencieux ou non silencieuse. Sur les autres plateformes, une \_ \_ Erreur du magasin de licences DRM E \_ \_ \_ est généralement retournée lorsque l’acquisition de la licence échoue. Le nouveau code d’erreur est destiné à distinguer l’échec d’acquisition de licence des autres conditions d’échec où une \_ \_ erreur de magasin de licences DRM E \_ \_ \_ a été générée.

La méthode recommandée pour gérer ces erreurs lorsqu’elles sont retournées après une tentative d’acquisition de licence en mode silencieux est indiquée dans l’extrait de code suivant :


```C++
if( hrStatus == NS_E_DRM_LICENSE_NOTACQUIRED || 
    hrStatus == NS_E_DRM_LICENSE_STORE_ERROR )
{
  // Attempt non-silent license acquisition.
}
else if( hrStatus == NS_E_DRM_NEEDS_INDIVIDUALIZATION )
{
  // Individualize and then retry.
}
else if( FAILED(hrStatus) )
{
  // Display a helpful error message.
}
else
{
  // Success. Play content.
}
```



> [!Note]  
> DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Lecture des fichiers protégés**](reading-protected-files.md)
</dt> </dl>

 

 




