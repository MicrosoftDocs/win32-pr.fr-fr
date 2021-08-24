---
title: Conception des extensions de classe d’assistance NDF
description: Cette rubrique a pour but de fournir des conseils génériques par le biais du processus de développement d’extension de classe d’assistance.
ms.assetid: f5dbd198-7d22-4e7e-830e-6753e9f4d6c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 474a9f4ade01fe98a8db30568aa6a7c4978156d2c791747353071f020af27605
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802359"
---
# <a name="designing-ndf-helper-class-extensions"></a>Conception des extensions de classe d’assistance NDF

Cette rubrique a pour but de fournir des conseils génériques par le biais du processus de développement d’extension de classe d’assistance. Les instructions de cette rubrique s’appliquent à toutes les extensions de classe d’assistance. pour obtenir des instructions plus spécifiques, consultez [Windows Class helper Platform extensible helper Class](windows-filtering-platform-extensible-helper-class.md) et [802,11 Wireless diagnostics extensible helper classes](802-11-wireless-diagnostics-extensible-helper-classes.md).

## <a name="extending-ndf-functionality"></a>Extension de la fonctionnalité NDF

Windows Vista et versions ultérieures sont fournis avec diverses classes d’assistance déjà implémentées qui peuvent diagnostiquer et réparer un large éventail de problèmes. Dans certains cas, toutefois, les développeurs tiers peuvent souhaiter étendre ces classes d’assistance pour diagnostiquer et résoudre les problèmes spécifiques à leurs produits et implémentations particuliers.

Les classes d’assistance Microsoft NDF suivantes sont extensibles.

-   [Plateforme de filtrage Windows](windows-filtering-platform-extensible-helper-class.md)
-   [Sécurité sans fil](802-11-wireless-diagnostics-extensible-helper-classes.md)

## <a name="implementing-a-helper-class-extension"></a>Implémentation d’une extension de classe d’assistance

Microsoft fournit deux interfaces qui peuvent être utilisées pour développer des extensions de classe d’assistance NDF.

L’interface [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) est appelée par NDF pour confirmer qu’elle contient toutes les informations requises et qu’elle a choisi la classe d’assistance appropriée. Pour ce faire, elle est effectuée via la méthode [**GetAttributeInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelperinfo-getattributeinfo) .

L’interface [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) est appelée par NDF pour la plupart des activités qui se produisent pendant la procédure de diagnostic. Plusieurs de ses méthodes sont requises, mais d’autres sont facultatives pour des utilisations spécifiques.

Les méthodes requises incluent [**Initialize**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize) et [**GetDiagnosticsInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getdiagnosticsinfo). NDF appelle **Initialize** pour envoyer des paramètres de clé à l’extension de la classe d’assistance pour initialiser son état d’instance. **GetDiagnosticsInfo** fournit une estimation de la durée pendant laquelle le diagnostic peut prendre et s’il nécessite l’emprunt d’identité du contexte de l’utilisateur d’origine.

Une autre méthode, [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth), est appelée pour effectuer un diagnostic sur le composant réseau correspondant à la classe d’assistance. [**Cancel**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-cancel) est appelé quand NDF détermine qu’un diagnostic ou une réparation en cours doit être arrêté. Le [**nettoyage**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-cleanup) permet à NDF de libérer des ressources NDF utilisées par l’extension de la classe d’assistance depuis que l’appel à [**Initialize**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize) a été effectué.

Pour plus d’informations sur les autres méthodes, consultez [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper).

Les extensions de classe d’assistance NDF sont utilisées pour diagnostiquer et résoudre les problèmes de connectivité associés à une application ou un composant spécifique. Ils valident également la réussite ou l’échec d’une tentative de résolution.

Les développeurs qui envisagent l’implémentation d’une extension de classe d’assistance doivent effectuer les tâches suivantes.

-   Identifiez les scénarios d’utilisateur dans lesquels les actions de diagnostic et de réparation sont utiles.
-   Fournir des solutions aux problèmes de connectivité rencontrés fréquemment.
-   Si une extension de classe d’assistance est requise, définissez un modèle d’intégrité de composant utilisé pour représenter l’état d’intégrité du composant dans NDF.

## <a name="identify-user-scenarios"></a>Identifier les scénarios utilisateur

Le test et l’utilisation d’une application ont peut-être déjà fourni des modèles pouvant être détectés qu’une extension de classe d’assistance peut être en mesure de diagnostiquer et éventuellement de réparer. Les développeurs d’applications peuvent utiliser ces données pour déterminer les problèmes de connectivité les plus importants à résoudre et pour identifier les scénarios utilisateur dans lesquels des problèmes de connectivité sont susceptibles de se produire.

La détermination de la cause racine de chaque problème est essentielle dans cette partie du processus. Cela peut nécessiter des recherches approfondies, mais permet de créer des logiciels qui sont beaucoup plus faciles à utiliser par les utilisateurs et les administrateurs. Si une cause racine n’est pas identifiée, il devient difficile, voire impossible, d’offrir la résolution des problèmes à l’aide de l’extension de classe d’assistance.

## <a name="provide-resolutions"></a>Fournir des solutions

Une fois qu’une équipe de développement a identifié les causes racines des problèmes associés à son logiciel, l’étape suivante consiste à identifier les actions de résolution appropriées pour aider l’utilisateur à résoudre le problème aussi efficacement que possible.

Toutes les résolutions ne nécessitent pas la création d’une extension de classe d’assistance ou d’une action automatisée. Dans certains cas, l’équipe peut déterminer que la meilleure approche pour résoudre une cause racine est de corriger ou de mettre à jour le composant, de fournir du contenu d’aide supplémentaire pour le composant ou de développer d’autres stratégies qui offrent de meilleures solutions à long terme.

Pour les problèmes dans lesquels une action automatisée est idéale, la création d’une extension de classe d’assistance NDF est souvent une excellente solution.

Les extensions de classe d’assistance renvoient des informations sur les causes racines et les informations de réparation aux utilisateurs via NDF. Les chaînes utilisées pour décrire les causes racines et les informations de réparation doivent être simples et faciles à comprendre pour un utilisateur non technique. Pour plus d’informations sur ces chaînes, consultez [instructions de l’interface utilisateur pour les extensions de classe d’assistance NDF](user-interface-guidelines-for-ndf-helper-class-extensions.md).

## <a name="define-a-component-health-model"></a>Définir un modèle d’intégrité de composant

Les développeurs de logiciels doivent définir des niveaux d’intégrité associés à la facilité de gestion des problèmes de mise en réseau. Un modèle d’intégrité utilisé pour développer des classes d’assistance définit uniquement deux niveaux d’intégrité : intègre et non intègre. Ces niveaux peuvent également être appliqués aux extensions de classe d’assistance NDF.

Un composant sain indique une absence de problèmes. Un composant peut être considéré comme défectueux en raison de ses propres problèmes, ou en raison de problèmes survenant dans d’autres composants dont il dépend.



| Terme                                                                                                                             | Description                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span id="LowHealth"></span><span id="lowhealth"></span><span id="LOWHEALTH"></span>LowHealth<br/>                         | Cet état indique un niveau inacceptable d’échecs de ce composant, et que le composant est le problème.<br/>    |
| <span id="LowHealth_Below"></span><span id="lowhealth_below"></span><span id="LOWHEALTH_BELOW"></span>LowHealth ci-dessous<br/> | Cet état indique un niveau inacceptable d’échecs à partir d’un composant d’ordinateur local dont dépend ce composant.<br/> |



 

Lorsque le diagnostic a lieu à l’aide d’NDF, l’extension de la classe d’assistance est invitée à une série de questions pour déterminer son état d’intégrité. Si l’extension répond qu’elle n’est pas intègre, NDF demande de clarifier les questions, d’essayer de diagnostiquer le problème, son emplacement et l’emplacement suivant. Chaque classe d’assistance doit être en mesure de répondre à la question de l’intégrité faible afin de mieux diriger les activités de diagnostic appropriées.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Classe d’assistance extensible de la plateforme de filtrage](windows-filtering-platform-extensible-helper-class.md)
</dt> <dt>

[Classes d’assistance extensibles pour les diagnostics sans fil 802,11](802-11-wireless-diagnostics-extensible-helper-classes.md)
</dt> </dl>

 

 





