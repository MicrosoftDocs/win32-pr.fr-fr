---
title: Vue d’ensemble des instructions relatives aux conteneurs de contrôle et de contrôle
description: Vue d’ensemble des instructions relatives aux conteneurs de contrôle et de contrôle
ms.assetid: c4cf2409-0085-43e6-afa2-f9c03cc50565
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2658c691e13b0a78da82fa006ed22142082e2f7eb8b04d78992943a024487a8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120459"
---
# <a name="overview-of-control-and-control-container-guidelines"></a>Vue d’ensemble des instructions relatives aux conteneurs de contrôle et de contrôle

un contrôle ActiveX est essentiellement un objet OLE simple qui prend en charge l’interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . Il prend généralement en charge davantage d’interfaces pour offrir des fonctionnalités, mais toutes les interfaces supplémentaires peuvent être affichées comme facultatives et, par conséquent, un conteneur de contrôle ne doit pas reposer sur les interfaces supplémentaires prises en charge. En ne spécifiant pas d’interfaces supplémentaires qu’un contrôle doit prendre en charge, un contrôle peut cibler efficacement une zone de fonctionnalités particulière sans avoir à prendre en charge des interfaces particulières pour qualifier comme contrôle. Comme toujours avec OLE, qu’il s’agisse d’un contrôle ou d’un conteneur de contrôle, il ne doit jamais être supposé qu’une interface est disponible et que les conventions de vérification de retour standard doivent toujours être suivies. Il est important pour un conteneur de contrôle ou de contrôle de se dégrader normalement et d’offrir d’autres fonctionnalités si une interface requise n’est pas disponible.

un conteneur de contrôle ActiveX doit pouvoir héberger un contrôle ActiveX minimal ; Il prend également en charge un certain nombre d’interfaces supplémentaires, comme spécifié dans les [conteneurs](containers.md). Un conteneur peut éventuellement prendre en charge un certain nombre d’interfaces et de méthodes, regroupées dans des domaines fonctionnels appelés *catégories de composants*. Un conteneur peut prendre en charge n’importe quelle combinaison de catégories de composants, par exemple, une catégorie de composant existe pour la liaison de liaison et un conteneur peut ou non prendre en charge la fonctionnalité de liaison de liaison, en fonction des besoins du marché du conteneur. Si un contrôle a besoin de la prise en charge de la liaison de liaison d’un conteneur pour fonctionner, il entre dans le registre. Cela permet à un conteneur de contrôle d’insérer uniquement les contrôles qu’il sait qu’il peut héberger avec succès. il est important de noter que les catégories de composants sont spécifiées dans le cadre d’OLE et ne sont pas spécifiques aux contrôles ActiveX, l’architecture des contrôles utilise des catégories de composants pour identifier les zones de fonctionnalité qu’un composant OLE peut prendre en charge. Les catégories de composants ne sont pas cumulatives ou exclusives, donc un conteneur de contrôle peut prendre en charge une catégorie sans nécessairement en prendre en charge une autre.

Il est important pour les contrôles qui nécessitent des fonctionnalités facultatives, ou les fonctionnalités spécifiques à un certain conteneur d’être clairement empaquetées et commercialisées avec ces exigences. de même, les conteneurs qui offrent certaines fonctionnalités ou catégories de composants doivent être commercialisés et empaquetés pour offrir ces niveaux de prise en charge lors de l’hébergement de contrôles de ActiveX. Il est recommandé que les contrôles ciblent et testent avec autant de conteneurs que possible et se dégradent harmonieusement pour offrir des fonctionnalités moins nombreuses ou alternatives si les interfaces ou les méthodes ne sont pas disponibles. Dans le cas où un contrôle ne peut pas exécuter sa fonction de travail désignée sans la prise en charge d’une catégorie de composant, cette catégorie doit être entrée en tant qu’exigence dans le registre afin d’empêcher l’insertion du contrôle dans un conteneur inapproprié.

Ces instructions définissent les interfaces et les méthodes qu’un contrôle peut s’attendre à ce qu’un conteneur de contrôle prenne en charge, même si le contrôle doit toujours vérifier les valeurs de retour lors de l’utilisation de [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) ou d’autres méthodes pour obtenir des pointeurs vers ces interfaces. Un conteneur ne doit pas s’attendre à ce qu’un contrôle prenne en charge quelque chose d’autre que l’interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , et ces instructions identifient les interfaces qu’un contrôle peut prendre en charge et ce que signifie la présence d’une interface particulière.

## <a name="why-the-activex-control-and-control-container-guidelines-are-important"></a>pourquoi les directives de contrôle ActiveX et de conteneur de contrôle sont importantes

ActiveX Les contrôles sont devenus l’architecture principale permettant de développer des composants logiciels programmables pour une utilisation dans différents conteneurs, allant des outils de développement de logiciels aux outils de productivité des utilisateurs finaux. Pour qu’un contrôle fonctionne correctement dans un grand nombre de conteneurs, le contrôle doit être en mesure de prendre en compte certains niveaux de fonctionnalités minimum sur lesquels il peut reposer dans tous les conteneurs.

En suivant ces directives, les développeurs de contrôle et de conteneur rendent leurs contrôles et leurs conteneurs plus fiables et interopérables, et finalement, de meilleurs et plus de composants utilisables pour la création de solutions basées sur des composants.

## <a name="what-to-do-when-an-interface-you-need-is-not-available"></a>Que faire quand une interface dont vous avez besoin n’est pas disponible

Les programmes OLE doivent utiliser [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) pour acquérir des pointeurs d’interface et doivent vérifier la valeur de retour. Les applications OLE ne peuvent pas supposer en toute sécurité que **QueryInterface** fonctionnera correctement.

Cette exigence s’applique à toutes les applications OLE. Si l’interface demandée n’est pas disponible (autrement dit, [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) retourne E \_ nointerface), le contrôle ou le conteneur doit se dégrader normalement, même si cela signifie qu’il ne peut pas exécuter sa fonction de tâche désignée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[ActiveX Instructions relatives aux conteneurs de contrôle et de contrôle](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 




