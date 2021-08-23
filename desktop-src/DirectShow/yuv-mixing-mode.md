---
description: Mode de mixage YUV
ms.assetid: 296b1d96-1824-4000-8bec-158925555177
title: Mode de mixage YUV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 957c5345eb80576ad0371558bb60d0b6651221bd98d7830cb968f39c16330fb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290749"
---
# <a name="yuv-mixing-mode"></a>Mode de mixage YUV

cette rubrique s’applique à Windows XP Service Pack 2 ou version ultérieure.

à compter de Windows XP Service Pack 2, VMR prend en charge un mode de mixage appelé mode de mixage YUV. Ce mode est particulièrement utile pour les applications TV ou DVD avancées. Il intègre une partie de la puissance de VMR mixer pour améliorer les performances sur le matériel graphique de bas niveau qui utilise une conception d’architecture de mémoire unifiée. Le mode de mixage YUV est pris en charge sur VMR-7 et VMR-9.

**Avantages**

Le mode de mixage YUV présente plusieurs avantages en ce qui concerne le rendu des performances par rapport au mode de mixage RVB d’origine pris en charge par VMR :

-   Lorsque VMR est en mode de mixage YUV, toutes les opérations de composition de flux vidéo et de désentrelacement sont effectuées dans l’espace colorimétrique YUV. Les surfaces YUV requièrent généralement entre 50% et 60% de bande passante de mémoire que les surfaces RVB équivalentes.
-   La composition de désentrelacement et de flux est effectuée par un appel unique au pilote Graphics. Le pilote peut utiliser les fonctionnalités de multi-texturisation du matériel graphique, ce qui permet d’économiser davantage de bande passante en mémoire.

Même si une application vidéo peut utiliser le mode de mélange YUV, elle est principalement destinée à deux types d’applications de lecture vidéo :

1.  Applications TV qui affichent des sous-titres ou du télétexte.
2.  Les applications DVD affichent des données de sous-image de DVD ou des sous-titres.

**Restrictions**

Un certain nombre de restrictions sont appliquées par le VMR lorsqu’il est placé en mode de mixage YUV :

-   Le flux 0 (le flux connecté à la broche d’entrée 0) peut être progressif ou entrelacé ; tous les autres flux doivent être progressifs.
-   Le GUID \_ null (mode tissage) n’est pas autorisé pour le flux 0.
-   DeinterlacePref \_ tissage ne peut pas être utilisé comme mode de secours, car cela peut empêcher la création d’un appareil de désentrelacement. Le mode de mixage YUV requiert un appareil de désentrelacement, même si la vidéo entrante n’est pas entrelacée.
-   Aucune modification ne peut être apportée à la valeur alpha planaire associée à chaque flux d’entrée VMR.
-   L’utilisateur ne peut pas modifier l’ordre de plan des flux vidéo connectés. L’ordre de plan par défaut est issu de l’ordre du code confidentiel.
-   Le masquage des couleurs n’est pas pris en charge.
-   La broche d’entrée 0 doit recevoir le flux vidéo.
-   Les autres broches d’entrée peuvent uniquement recevoir des données de sous-flux vidéo, telles que des sous-images de DVD, des sous-titres ou du télétexte.
-   Les autres broches d’entrée peuvent uniquement accepter des formats YUV alpha par pixel, tels que AYUV, AI44 et IA44.
-   Aucune des broches d’entrée de VMR ne peut accepter des formats RVB.
-   Les images bitmap fournies par l’application ne peuvent plus être combinées avec la vidéo avant la présentation à l’écran.
-   Les sous-flux individuels ne peuvent pas être inversés horizontalement ou verticalement à l’aide des fonctions « rectangle de sortie » du mélangeur VMR. Le repositionnement et le redimensionnement du flux « normal » sont pris en charge.
-   La couleur d’arrière-plan de mixage (spécifiée par [**IVMRMixerControl :: SetBackgroundClr**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setbackgroundclr)) est toujours spécifiée dans l’espace de couleurs RVB, tout comme en mode de mélange RVB.

**Configuration**

Les applications doivent configurer explicitement VMR pour tirer parti du mode de mélange YUV ; le mode de mixage RVB d’origine reste le mode de mixage par défaut. Pour activer le mode de mixage YUV dans VMR-7, appelez [**IVMRMixerControl :: SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) avec l' \_ indicateur RenderTargetYUV MixerPref. Cet appel doit être effectué avant que l’une des broches d’entrée de VMR soit connectée. Pour activer le mode de mixage YUV dans VMR-9, appelez [**IVMRMixerControl9 :: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) avec l' \_ indicateur RenderTargetYUV MixerPref9.

La seule façon de déterminer si VMR-7 prend en charge le nouveau mode de mixage YUV consiste à essayer de définir le VMR dans ce mode. Si l’appel est effectué, vous pouvez toujours remettre VMR en mode de mixage RVB si nécessaire. Une fois qu’elle est définie en mode de mixage YUV, le VMR peut uniquement être rétabli en mode mixte RVB après que toutes les broches d’entrée ont été déconnectées.

En mode mélange YUV, vous pouvez réduire la charge sur l’unité de traitement graphique (GPU) en appliquant les indicateurs suivants dans la méthode **SetMixingPrefs** :



| Indicateur                                                                                 | Description                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| VMR-7 : MixerPref \_ DynamicSwitchToBOBVMR-9 : MixerPref9 \_ DynamicSwitchToBOB<br/> | Basculez vers le désentrelacement Bob.                                     |
| VMR-7 : MixerPref \_ DynamicDecimateBy2VMR-9 : MixerPref \_ DynamicDecimateBy2<br/>  | Décimez l’image d’un facteur de 2 horizontalement et verticalement. |



 

Vous pouvez ajouter ou supprimer ces indicateurs pendant que le graphique de filtre est en cours d’exécution ; la modification est appliquée lorsque le mélangeur VMR compose la prochaine image vidéo. Les indicateurs ne s’excluent pas mutuellement. Ces paramètres réduisent la qualité de l’image. en général, vous les appliquez uniquement lorsque la qualité vidéo est moins importante, par exemple si la vidéo est lue dans une petite partie de l’interface utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du mode de mixage VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 




