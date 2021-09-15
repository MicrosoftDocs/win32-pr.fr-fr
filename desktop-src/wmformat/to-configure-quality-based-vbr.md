---
title: Pour configurer Quality-Based VBR
description: Pour configurer Quality-Based VBR
ms.assetid: 077a18c5-1895-4241-8c31-5f7caf38b22e
keywords:
- flux, configuration des flux VBR
- flux, débit binaire variable (VBR)
- Vitesse de transmission variable (VBR), flux
- VBR (vitesse de transmission variable), flux
- flux, configuration du VBR basé sur la qualité
- Vitesse de transmission variable (VBR), configuration de la qualité
- VBR (vitesse de transmission variable), configuration de la qualité
- profils, configuration du VBR basé sur la qualité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0b7a6ecb83c7242f82f5626a086c8aba23881f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404461"
---
# <a name="to-configure-quality-based-vbr"></a>Pour configurer Quality-Based VBR

Vous pouvez utiliser l’encodage VBR (Quality bit rate) sur un flux pour spécifier un niveau de qualité qui sera conservé pour l’ensemble du flux, indépendamment des exigences de vitesse de transmission qui en résultent.

Pour les flux vidéo VBR basés sur la qualité, vous devez spécifier un niveau de qualité compris entre 1 et 100, 100 représentant la qualité la plus élevée. À l’heure actuelle, il n’existe que 30 paramètres de qualité discrets. Les niveaux de qualité suivants sont équivalents aux paramètres de qualité discrets : 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, 100. Les nombres entre deux valeurs consécutives dans la liste précédente sont équivalents au même paramètre de qualité que le nombre inférieur. Par exemple, 1 et 4 sont répertoriés, si bien que 2 et 3 produisent le même paramètre de qualité que 1.

Pour les flux audio, vous pouvez énumérer les modes disponibles et récupérer un objet de configuration de flux. Pour plus d’informations, consultez [pour énumérer des formats de codec](to-enumerate-codec-formats.md).

Lorsque vous utilisez une vidéo VBR basée sur la qualité, vous devez définir le membre **dwBitrate** de la structure [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) sur une valeur positive. Cette valeur n’est pas utilisée par le writer, mais le passage de zéro ou d’un nombre négatif peut provoquer des erreurs lors de l’écriture.

Pour configurer un flux dans un profil à encoder avec un VBR basé sur la qualité, procédez comme suit.

1.  Créez un objet de gestionnaire de profils en appelant la fonction [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .
2.  Ouvrez un profil existant auquel vous souhaitez ajouter la prise en charge VBR. Pour plus d’informations sur l’ouverture des profils, consultez [utilisation des profils](working-with-profiles.md).
3.  Récupérez un objet de configuration de flux pour le flux que vous souhaitez utiliser en appelant [**IWMProfile :: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) ou [**IWMProfile :: GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).
4.  Obtenir un pointeur vers l’interface [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) de l’objet de configuration de flux en appelant **IWMStreamConfig :: QueryInterface**.
5.  Activez le VBR pour le flux en appelant [**IWMPropertyVault :: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) pour la propriété **g \_ wszVBREnabled** .
6.  Définissez le niveau de qualité pour le flux VBR en appelant **IWMPropertyVault :: SetProperty** pour la propriété **g \_ wszVBRQuality** .
7.  Affectez aux paramètres **g \_ wszVBRBitrateMax** et **g \_ WszVBRBufferWindowMax** la valeur zéro avec **IWMPropertyVault :: SetProperty**.
8.  Enregistrez les modifications apportées au flux en appelant [**IWMProfile :: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).
9.  Enregistrez le profil ou transmettez-le à l’objet Writer et commencez l’écriture.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Configuration de VBR Flux**](configuring-vbr-streams.md)
</dt> </dl>

 

 




