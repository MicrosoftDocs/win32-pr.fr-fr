---
title: Utilisation des niveaux de protection de sortie
description: Utilisation des niveaux de protection de sortie
ms.assetid: ec5982cd-0b87-4081-98e2-ab2d102a36d8
keywords:
- Windows Media Format SDK, niveaux de protection de sortie (OPL)
- Windows Media Format SDK, niveaux de protection
- ASF (Advanced Systems Format), niveaux de protection de sortie (OPL)
- ASF (format des systèmes avancés), niveaux de protection de la sortie (OPL)
- ASF (Advanced Systems Format), niveaux de protection
- ASF (format des systèmes avancés), niveaux de protection
- ASF (Advanced Systems Format), plusieurs licences
- ASF (Advanced Systems Format), plusieurs licences
- gestion des droits numériques (DRM), niveaux de protection de sortie (OPL)
- DRM (gestion des droits numériques), niveaux de protection de sortie (OPL)
- gestion des droits numériques (DRM), niveaux de protection
- DRM (gestion des droits numériques), niveaux de protection
- gestion des droits numériques (DRM), évaluation des niveaux de protection de sortie (OPL)
- DRM (Digital Rights Management), évaluation des niveaux de protection de sortie (OPL)
- gestion des droits numériques (DRM), plusieurs licences
- DRM (gestion des droits numériques), plusieurs licences
- niveaux de protection de sortie (OPL)
- OPL (niveaux de protection de sortie)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aab7023cc8285e5f3993aac69c57deca9675d9dd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314221"
---
# <a name="working-with-output-protection-levels"></a>Utilisation des niveaux de protection de sortie

Les licences créées à l’aide du kit de développement logiciel (SDK) Windows Media Rights Manager 10 peuvent spécifier des restrictions d’action à l’aide des niveaux de protection de sortie (OPLs). OPLs permet à un créateur de licence d’autoriser certaines actions uniquement sur des appareils avec des technologies spécifiques. Les avantages de l’utilisation de OPLs sont que vous bénéficiez d’une plus grande flexibilité pour créer des restrictions de licence que les versions précédentes. En outre, les OPLs sont extensibles pour s’adapter aux futures technologies. Vous pouvez prendre en charge ces licences dans vos applications à l’aide des méthodes de l’interface [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2) .

Pour lire les fichiers qui sont protégés par une licence qui spécifie OPLs, vous devez vérifier la OPL de l’action souhaitée. La technologie de sortie utilisée par votre application doit être autorisée par le OPL dans la licence. Par exemple, certaines licences pour le contenu audio protégé peuvent nécessiter l’utilisation d’un chemin d’accès audio sécurisé pour le lire.

## <a name="configuring-the-reader-to-evaluate-output-protection-levels"></a>Configuration du lecteur pour évaluer les niveaux de protection de sortie

Avant de pouvoir vérifier OPLs pour les fichiers chargés dans le lecteur, vous devez appeler la méthode [**IWMDRMReader2 :: SetEvaluateOutputLevelLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses) , en passant **true** pour le paramètre *fEvaluate* . Si vous n’appelez pas cette méthode, les licences qui requièrent des OPLs ne sont pas visibles par votre application.

## <a name="evaluating-copy-output-protection-levels"></a>Évaluation des niveaux de protection de copie de sortie

Pour obtenir les niveaux de protection de sortie de l’action de copie, appelez la méthode [**IWMDRMReader2 :: GetCopyOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getcopyoutputlevels) . Les données que vous recevez de l’appel sont stockées dans une structure [**\_ \_ OPL de copie DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl) . La structure contient un niveau de protection de sortie de base, qui spécifie le niveau de sortie minimal pour l’action de copie dans la licence. Toutefois, la \_ structure OPL de la copie DRM \_ contient également deux listes d’identificateurs de technologie : une pour les technologies autorisées qui sont évaluées à un OPL inférieur à la base et une pour les technologies évaluées égales ou supérieures à celles du OPL de base, mais qui sont limitées par la licence. Vous devez vérifier les inclusions et les exclusions pour vous assurer que la technologie utilisée par votre application est autorisée par la licence.

## <a name="evaluating-play-output-protection-levels"></a>Évaluation des niveaux de protection de sortie de lecture

Pour obtenir les niveaux de protection de sortie de l’action Play, appelez la méthode [**IWMDRMReader2 :: GetPlayOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels) . Les données que vous recevez de l’appel sont stockées dans une structure de [**\_ lecture DRM \_ OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl) . La structure contient plusieurs autres structures. Les niveaux de protection de sortie de base pour l’action de lecture sont stockés dans une structure de [**niveaux de protection de \_ \_ sortie \_ \_ DRM minimum**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) (le membre **minOPL** de **DRM \_ Play \_ OPL**), qui définit le OPL minimal requis pour lire le contenu dans divers formats. Vous devez vérifier le type des formats de sortie fournis par votre application.

La **structure \_ \_ OPL de la lecture DRM** définit deux types de restrictions : les identificateurs d’échantillonnage et de protection de sortie vidéo autorisés.

L’échantillonnage obligatoire est défini sous la forme d’une liste d’identificateurs de technologie de sortie (le membre **oplIdDownsample** de la fonction **DRM \_ Play \_ OPL**) qui, s’il est utilisé, peut recevoir le contenu pour lecture uniquement si le contenu est d’abord abaissé à une vitesse de transmission inférieure.

Les identificateurs de protection de sortie vidéo autorisés sont définis comme une liste de technologies de sortie vidéo avec les informations de configuration de chacune.

## <a name="handling-multiple-licenses"></a>Gestion de plusieurs licences

Certains fichiers peuvent être associés à plusieurs licences dans le magasin de licences local. Lorsque vous évaluez OPLs pour un fichier que vous lisez, vous pouvez rechercher d’autres licences en appelant la méthode [**IWMDRMReader2 :: TryNextLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense) . Vous devez continuer à essayer les licences jusqu’à ce que vous en trouviez une qui autorise l’action que vous voulez effectuer ou jusqu’à ce que TryNextLicense retourne DRM \_ S \_ false, ce qui indique qu’il n’y a plus de licences.

Dans certains cas, un fichier peut avoir une licence associée qui requiert un OPL que votre application ne peut pas prendre en charge. Dans ce cas, il est important de vérifier la présence de licences supplémentaires, car il existe une licence qui ne spécifie pas OPLs.

**Remarque** DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Activation de la prise en charge de DRM**](enabling-drm-support.md)
</dt> <dt>

[**Interface IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)
</dt> </dl>

 

 




