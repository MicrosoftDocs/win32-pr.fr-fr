---
title: Utilisation des données de fonctionnalités Direct3D 11 pour compléter les niveaux de fonctionnalité Direct3D
description: Découvrez comment vérifier la prise en charge d’appareils pour les fonctionnalités facultatives, notamment les fonctionnalités qui ont été ajoutées dans les versions récentes de Windows.
ms.assetid: 91D9706A-47C5-4220-8AC7-167095E74F74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dcc770812281ea89e8ebb68065aa68a00e1887d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315593"
---
# <a name="using-direct3d-11-feature-data-to-supplement-direct3d-feature-levels"></a>Utilisation des données de fonctionnalités Direct3D 11 pour compléter les niveaux de fonctionnalité Direct3D

Découvrez comment vérifier la prise en charge d’appareils pour les fonctionnalités facultatives, notamment les fonctionnalités qui ont été ajoutées dans les versions récentes de Windows.

Les [niveaux de fonctionnalité Direct3D](overviews-direct3d-11-devices-downlevel-intro.md) indiquent des ensembles bien définis de fonctionnalités GPU qui correspondent approximativement à différentes générations de matériel graphique. Cela simplifie grandement la vérification des capaibilities matériels et fournit également une expérience cohérente sur un large éventail d’appareils différents.

Pour tenir compte de la variance entre les différentes implémentations matérielles, y compris le matériel hérité, le matériel mobile et le matériel moderne, certaines fonctionnalités sont considérées comme facultatives. La prise en charge de ces fonctionnalités peut être déterminée en appelant [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) et en fournissant la structure de données de la fonctionnalité d3d11 pertinente \_ \_ \_ \* . Cette rubrique décrit les différentes fonctionnalités facultatives de Direct3D 11, comment certaines d’entre elles fonctionnent ensemble et comment vous pouvez éviter de vérifier toutes les fonctionnalités facultatives.

## <a name="how-to-check-for-optional-feature-support"></a>Comment vérifier la prise en charge des fonctionnalités facultatives

Appelez [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport), en fournissant la structure qui représente la fonctionnalité facultative que vous souhaitez utiliser. Si la méthode retourne la valeur **\_ OK**, cela signifie que vous êtes sur une version du runtime Direct3D qui prend en charge la fonctionnalité facultative. Si elle retourne **E \_ INVALIDARG**, cela signifie que vous êtes sur une version du runtime Direct3D 11 avant l’ajout de la fonctionnalité facultative. cela signifie que la fonctionnalité facultative n’est pas disponible, ainsi que toutes les autres fonctionnalités facultatives introduites dans la même version de Direct3D 11 ou version ultérieure.

## <a name="can-i-minimize-the-work-required-for-feature-support-checks"></a>Puis-je réduire le travail requis pour les vérifications de prise en charge des fonctionnalités ?

En plus d’avoir le bon Runtime Direct3D 11 (généralement associé à une version de Windows), le pilote Graphics doit également être suffisamment récent pour prendre en charge la fonctionnalité facultative. Les spécifications WDDM nécessitent la prise en charge de fonctionnalités facultatives si le matériel peut le prendre en charge. Ainsi, lorsqu’un pilote Graphics prend en charge l’une des fonctionnalités facultatives qui ont été ajoutées dans une version particulière de Windows, cela signifie généralement que le pilote Graphics prend en charge les autres fonctionnalités ajoutées à cette version de Windows. Par exemple, si un pilote de périphérique prend en charge les ombres sur le niveau de fonctionnalité 9, vous savez que le pilote de périphérique est au moins WDDM 1,2.

**Remarque**    Si un périphérique Microsoft Direct3D prend en charge le [niveau de fonctionnalité](overviews-direct3d-11-devices-downlevel-intro.md) 11,1, toutes les fonctionnalités facultatives indiquées par les [**\_ \_ \_ \_ options d3d11 des données de la fonctionnalité d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) sont prises en charge automatiquement, à l’exception de **SAD4ShaderInstructions** et **ExtendedDoublesShaderInstructions**.

Le runtime définit toujours les regroupements de membres suivants de manière identique. Autrement dit, toutes les valeurs d’un regroupement sont **true** ou **false** :

-   **DiscardAPIsSeenByDriver** et **FlagsForUpdateAndCopySeenByDriver**
-   **Clearview**, **CopyWithOverlap**, **ConstantBufferPartialUpdate**, **ConstantBufferOffsetting** et **MapNoOverwriteOnDynamicConstantBuffer**
-   **MapNoOverwriteOnDynamicBufferSRV** et **MultisampleRTVWithForcedSampleCountOne**

**Options de niveau de fonctionnalité 11,2 ([**\_ fonctionnalité d3d11 \_ d3d11 \_ options1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature)) :** les fonctionnalités facultatives indiquées par ce champ sont indépendantes et doivent être vérifiées individuellement.

### <a name="feature-support-on-windows-rt-81-and-windows-phone-81-devices"></a>Prise en charge des fonctionnalités sur les appareils Windows RT 8,1 et Windows Phone 8,1

Les périphériques tablette Windows RT peuvent prendre en charge un large éventail de niveaux de fonctionnalités et de fonctionnalités facultatives, sont optimisés pour réduire la consommation d’énergie et utilisent des graphiques intégrés plutôt que des GPU discrètes. Les applications du Windows Store pour les appareils ARM doivent prendre en charge le niveau de fonctionnalité 9,1. Les applications DirectX pour Windows RT doivent tirer parti des fonctionnalités facultatives qui peuvent économiser de la puissance et des cycles, comme l’instanciation simple, quand elles sont disponibles.

Windows Phone 8 appareils mobiles prennent en charge le niveau de fonctionnalité 9,3 avec des fonctionnalités facultatives spécifiques. Consultez [niveau de fonctionnalité Direct3D 9 \_ 3 pour Windows Phone 8](/previous-versions/windows/apps/jj714085(v=vs.105)).

## <a name="what-are-the-direct3d-11-optional-features"></a>Quelles sont les fonctionnalités facultatives de Direct3D 11 ?

Le reste de cet article décrit les fonctionnalités facultatives disponibles dans Direct3D 11,2. Les fonctionnalités sont décrites dans l’ordre chronologique selon lesquelles elles ont été ajoutées pour vous permettre d’obtenir un sens pour les fonctionnalités qui se trouvent dans différentes versions de Direct3D 11.

## <a name="optional-compute-shader-support-for-feature-level-10"></a>Prise en charge facultative du nuanceur de calcul pour le niveau de fonctionnalité 10

La fonctionnalité suivante est toujours disponible pour les appareils de niveau de fonctionnalité 10 :

**[**D3d11 \_ Données des fonctionnalités \_ \_ D3D10 \_ X \_ \_ options matérielles**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options):** si la **valeur est true**, l’appareil prend en charge les nuanceurs de calcul. Cela prend en charge les mémoires tampons brutes et structurées.

Lorsque l’appareil de niveau de fonctionnalité 10 \_ 0 ou 10 \_ 1 prend en charge cette fonctionnalité, il n’est pas garanti que l’appareil prenne en charge le nuanceur de calcul 4,1. Les applications doivent être prêtes à revenir à un nuanceur de calcul 4,0 si [**ID3D11Device :: CreateComputeShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader) lève une exception avec un programme de nuanceur de calcul 4,1.

## <a name="optional-capabilities-for-feature-level-9"></a>Fonctionnalités facultatives pour le niveau de fonctionnalité 9

Les fonctionnalités suivantes sont ajoutées pour le niveau de fonctionnalité 9 à partir de Windows 8 :

**[**D3d11 \_ Feature \_ Data \_ d3d9 \_ options**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options):** indique la prise en charge de l’adressage de texture de retour à la ligne avec des textures non-de-2. Si cela est pris en charge, le \_ \_ \_ mode d’adresse de texture d3d11 \_ encapsulé peut être utilisé avec ces textures.

**[**\_ \_ \_ \_ \_ Prise en charge des clichés instantanés d3d9 des données de fonctionnalités d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support):** indique la prise en charge des échantillonneurs de comparaison dans les nuanciers du modèle de nuanceur 4,0 niveaux 9 \_ x. Il est utilisé pour le test de profondeur dans les nuanceurs de pixels, ce qui permet la prise en charge des techniques courantes telles que le mappage et les stencils fantômes.

La fonctionnalité suivante a été ajoutée pour les appareils de niveau de fonctionnalité 9 à partir de Windows 8.1 :

**[**\_ \_ \_ \_ \_ \_ Prise en charge de l’instanciation simple des données de fonctionnalités d3d11 d3d9**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support):** indique la prise en charge des fonctionnalités d’instanciation simples qui peuvent être disponibles sur le matériel DirectX 9. L’instanciation simple signifie que tous les membres **InstanceDataStepRate** des structures [**\_ \_ \_ desc des éléments d’entrée d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_input_element_desc) utilisés pour définir la disposition d’entrée doivent être égaux à 1. Les appareils qui prennent en charge le niveau de fonctionnalité 9,3 ou ultérieur incluent déjà la prise en charge complète de l’instanciation.

## <a name="optional-floating-point-precision-support-for-shader-programs"></a>Prise en charge de la précision en virgule flottante facultative pour les programmes de nuanceur

**[**\_ \_ \_ \_ \_ \_ Prise en charge**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support)de la précision minimale du nuanceur de données de la fonctionnalité d3d11 :** les champs de ce struct indiquent la longueur des nombres à virgule flottante lorsque la précision minimale est activée, ou 0 si seule une précision de virgule flottante de 32 bits est prise en charge.

Pour les appareils de niveau de fonctionnalité 9, la précision minimale du nuanceur de sommets peut être différente de celle du nuanceur de pixels. La précision du nuanceur de sommets est indiquée dans le champ **AllOtherShaderStagesMinPrecision** .

**[**\_ Données de fonctionnalités d3d11 \_ \_ double**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles):** les appareils de niveau de fonctionnalité 11 peuvent prendre en charge les calculs à double précision dans les programmes de nuanceur 5,0. La prise en charge des calculs à double précision au sein du nuanceur signifie que les valeurs float peuvent être converties en valeurs doubles dans le programme de nuanceur de calcul, ce qui offre l’avantage d’un calcul de précision plus élevé au sein de chaque passe de nuanceur. Les nombres à double précision doivent être reconvertis en valeurs float avant d’être écrits dans la mémoire tampon de sortie. Notez que la Division à double précision n’est pas nécessairement prise en charge.

## <a name="additional-capabilities-for-direct3d-112"></a>Fonctionnalités supplémentaires pour Direct3D 11,2

Direct3D 11,2 ajoute quatre nouvelles fonctionnalités facultatives qui peuvent être prises en charge par les périphériques Direct3D 11. Ces fonctionnalités se trouvent dans la structure de données de la [**\_ fonctionnalité d3d11 \_ \_ d3d11 \_ options1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) :

**TiledResourcesTier :** Indique la prise en charge des ressources en mosaïque et indique le niveau de niveau pris en charge.

**MinMaxFiltering :** Indique la prise en charge des \_ \_ options de filtrage minimum du filtre D3D11 \_ \* et d3d11 \_ filtre \_ maximal \_ \* , qui comparent le résultat du filtrage à la valeur minimale (ou maximale). Consultez [**\_ filtre d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_filter).

**ClearViewAlsoSupportsDepthOnlyFormats :** Indique la prise en charge de l’effacement des vues de ressources de mémoire tampon de profondeur.

**MapOnDefaultBuffers :** Indique la prise en charge du mappage des mémoires tampons cibles de rendu créées avec l’indicateur d' **\_ utilisation \_ par défaut d3d11** .

## <a name="tile-based-rendering"></a>Rendu en mosaïque

**[**\_ \_ \_ \_ Informations sur l’architecture des données de la fonctionnalité d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info):** indique si le périphérique graphique effectue le rendu des commandes et effectue par défaut un rendu basé sur les mosaïques. Cela peut être utilisé comme indicateur pour l’optimisation du moteur graphique.

## <a name="optional-features-for-development-and-debugging"></a>Fonctionnalités facultatives pour le développement et le débogage

**D3d11 \_ OPTIONS de d3d11 de données de fonctionnalité \_ \_ \_ ::D iscardapisseenbydriver :** vous pouvez surveiller ce membre pendant le développement pour éliminer les pilotes hérités sur le matériel où [**DiscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) et [**DiscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) peuvent autrement avoir été bénéfiques.

**[**\_ \_ \_ \_ Prise en charge des marqueurs de données de fonctionnalités d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_marker_support):** cela est pris en charge si le matériel et le pilote prennent en charge le marquage des données pour le profilage GPU.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Appareils](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 