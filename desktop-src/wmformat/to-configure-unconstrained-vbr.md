---
title: Pour configurer le VBR sans contrainte
description: Pour configurer le VBR sans contrainte
ms.assetid: 69ef951f-d08b-401b-a285-2ffdf43ea35d
keywords:
- flux, configuration des flux VBR
- flux, débit binaire variable (VBR)
- Vitesse de transmission variable (VBR), flux
- VBR (vitesse de transmission variable), flux
- flux, configuration du VBR sans contrainte
- Vitesse de transmission variable (VBR), configuration sans contrainte
- VBR (vitesse de transmission variable), configuration sans contrainte
- profils, configuration du VBR sans contrainte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b24c022c79bb38414ab201db11abd0cf260dfafe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522997"
---
# <a name="to-configure-unconstrained-vbr"></a>Pour configurer le VBR sans contrainte

Vous pouvez utiliser l’encodage VBR (variable bit rate) sans contrainte sur un flux pour spécifier une vitesse de transmission moyenne qui sera maintenue dans le contenu encodé. Le VBR sans contrainte diffère du CBR normal dans la mesure où la variance de la vitesse de transmission de l’ensemble du flux peut être supérieure.

La vitesse de transmission du flux, définie avec [**IWMStreamConfig :: SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate), est utilisée comme taux binaire moyen souhaité. Lorsque l’encodage du flux est terminé, vous pouvez utiliser [**IWMPropertyVault :: GetPropertyByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-getpropertybyname) pour récupérer deux propriétés supplémentaires : **g \_ wszVBRPeak** et **g \_ wszBufferAverage**. Ces propriétés décrivent respectivement le taux de bits de pointe du contenu encodé et la fenêtre de mémoire tampon moyenne du contenu.

Le VBR sans contrainte doit être utilisé conjointement avec l’encodage en deux passes. L’encodage en deux passes n’est pas défini dans le profil. Vous devez configurer le writer pour effectuer une étape de prétraitement avant d’écrire le flux. Pour plus d’informations sur l’utilisation de l’encodage en deux passes, consultez [utilisation de l’encodage Two-Pass](using-two-pass-encoding.md).

Pour configurer un flux dans un profil à encoder avec un VBR non restreint, procédez comme suit :

1.  Créez un objet de gestionnaire de profils en appelant la fonction [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .
2.  Ouvrez un profil existant auquel vous souhaitez ajouter la prise en charge VBR. Pour plus d’informations sur l’ouverture des profils, consultez [utilisation des profils](working-with-profiles.md).
3.  Récupérez un objet de configuration de flux pour le flux que vous souhaitez utiliser en appelant [**IWMProfile :: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) ou [**IWMProfile :: GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).
4.  Obtenir un pointeur vers l’interface [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) de l’objet de configuration de flux en appelant **IWMStreamConfig :: QueryInterface**.
5.  Activez le codage VBR pour le flux en appelant [**IWMPropertyVault :: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) pour la propriété **g \_ wszVBREnabled** .
6.  Affectez aux paramètres **g \_ wszVBRBitrateMax** et **g \_ WszVBRBufferWindowMax** la valeur zéro avec **IWMPropertyVault :: SetProperty**.
7.  Enregistrez les modifications apportées au flux en appelant [**IWMProfile :: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).
8.  Enregistrez le profil ou transmettez-le à l’objet Writer.
9.  Configurez l’enregistreur pour effectuer une passe de prétraitement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Configuration de VBR Flux**](configuring-vbr-streams.md)
</dt> </dl>

 

 




