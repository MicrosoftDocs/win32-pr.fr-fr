---
title: Pour configurer le VBR restreint
description: Pour configurer le VBR restreint
ms.assetid: a39e7628-0211-48ad-94e5-5003203f30be
keywords:
- flux, configuration des flux VBR
- flux, débit binaire variable (VBR)
- Vitesse de transmission variable (VBR), flux
- VBR (vitesse de transmission variable), flux
- flux, configuration du VBR restreint
- Vitesse de transmission variable (VBR), configuration avec restriction
- VBR (vitesse de transmission variable), configuration avec restriction
- profils, configuration du VBR restreint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98d4e2a1bbea1b724fdde1cc820f19caf9dd77be
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104030928"
---
# <a name="to-configure-constrained-vbr"></a>Pour configurer le VBR restreint

Vous pouvez utiliser l’encodage VBR (variable bit rate) sur un flux pour spécifier un débit binaire moyen qui sera maintenu dans le contenu encodé. Vous spécifiez également la vitesse de transmission maximale du flux et la fenêtre de mémoire tampon maximale requise.

Vous ne pouvez pas savoir quel est le taux de bits moyen pour un flux VBR restreint avant l’encodage, mais vous pouvez utiliser une estimation approximative. En règle générale, la vitesse de transmission maximale que vous spécifiez se termine deux à trois fois la vitesse de transmission moyenne.

Le VBR restreint doit être utilisé conjointement avec l’encodage en deux passes. L’encodage en deux passes n’est pas défini dans le profil. Vous devez configurer le writer pour effectuer une étape de prétraitement avant d’écrire le flux. Pour plus d’informations sur l’utilisation de l’encodage en deux passes, consultez [utilisation de l’encodage Two-Pass](using-two-pass-encoding.md).

Pour configurer un flux dans un profil afin d’utiliser l’encodage VBR restreint, procédez comme suit.

1.  Créez un objet de gestionnaire de profils en appelant la fonction [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .
2.  Ouvrez un profil existant auquel vous souhaitez ajouter la prise en charge VBR. Pour plus d’informations sur l’ouverture des profils, consultez [utilisation des profils](working-with-profiles.md).
3.  Récupérez un objet de configuration de flux pour le flux que vous souhaitez utiliser en appelant [**IWMProfile :: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) ou [**IWMProfile :: GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).
4.  Obtenir un pointeur vers l’interface [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) de l’objet de configuration de flux en appelant **IWMStreamConfig :: QueryInterface**.
5.  Activez le codage VBR pour le flux en appelant [**IWMPropertyVault :: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) pour la propriété **g \_ wszVBREnabled** .
6.  Utilisez des appels à **IWMPropertyVault :: SetProperty** pour définir les valeurs maximales souhaitées pour les propriétés **g \_ wszVBRBitrateMax** et **g \_ wszVBRBufferWindowMax** .
7.  Enregistrez les modifications apportées au flux en appelant [**IWMProfile :: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).
8.  Enregistrez le profil ou transmettez-le à l’objet Writer.
9.  Configurez l’enregistreur pour effectuer une passe de prétraitement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Configuration de flux VBR**](configuring-vbr-streams.md)
</dt> </dl>

 

 




