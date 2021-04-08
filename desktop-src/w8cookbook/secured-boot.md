---
title: Logiciel anti-programme malveillant à lancement anticipé (ELAM)
description: Logiciel anti-programme malveillant à lancement anticipé (ELAM)
ms.assetid: 4064CD44-FC50-48DE-8490-F592ED21CB7E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c3e51d7fb009ffa0e85a59990b321fb38ad196
ms.sourcegitcommit: a93d3abaf4d6d45a6f0b87faed3f576b222b1745
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104042898"
---
# <a name="early-launch-antimalware"></a>Logiciel anti-programme malveillant à lancement anticipé (ELAM)

## <a name="platforms"></a>Plateformes

 **Clients** -Windows 8  
**Serveurs** -Windows Server 2012  

## <a name="description"></a>Description

Comme le logiciel anti-programme malveillant est devenu mieux et mieux adapté à la détection des programmes malveillants du runtime, les attaquants deviennent également mieux adaptés à la création de rootkits qui peuvent masquer la détection. La détection de programmes malveillants qui démarrent tôt au cours du cycle de démarrage est un défi que la plupart des fournisseurs sont tenus de faire face à la diligence. En règle générale, ils créent des piratages système qui ne sont pas pris en charge par le système d’exploitation hôte et qui peuvent entraîner le placement de l’ordinateur dans un état instable. Jusqu’à présent, Windows n’a pas fourni un bon moyen de détecter et de résoudre ces menaces de démarrage anticipé.

Windows 8 introduit une nouvelle fonctionnalité appelée démarrage sécurisé, qui protège la configuration et les composants de démarrage de Windows et charge un pilote ELAM (anti-programme malveillant) à lancement anticipé. Ce pilote démarre avant les autres pilotes de démarrage et permet l’évaluation de ces pilotes et aide le noyau Windows à déterminer s’ils doivent être initialisés.

## <a name="manifestation"></a>Manifestation

En étant lancé en premier par le noyau, ELAM est assuré d’être lancé avant tout logiciel tiers. il est donc en mesure de détecter les logiciels malveillants dans le processus de démarrage et de les empêcher de s’initialiser.

## <a name="mitigation"></a>Limitation des risques

Les pilotes de démarrage sont initialisés en fonction de la classification retournée par le pilote ELAM conformément à une stratégie d’initialisation. Par défaut, la stratégie initialise les pilotes connus et inconnus, mais n’initialise pas les pilotes incorrects connus. Un administrateur système peut spécifier une stratégie personnalisée via stratégie de groupe qui peut empêcher des pilotes inconnus d’initialiser ou peut activer des pilotes qui sont critiques pour le processus de démarrage, mais qui ont été falsifiés, le démarrage doit être initialisé.

## <a name="solution"></a>Solution

Un pilote ELAM doit s’inscrire pour les rappels de noyau afin d’obtenir des informations sur chaque pilote de démarrage lors de son initialisation. Le pilote ELAM peut ensuite retourner une classification pour chaque pilote. Ces fonctions sont requises :

-   [IoRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [IoUnRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)

Un pilote ELAM peut également s’inscrire pour les rappels du Registre. Cela permet au pilote ELAM d’inspecter les données de configuration utilisées par chaque pilote de démarrage. Le pilote ELAM peut ensuite bloquer ou modifier les données avant qu’elles ne soient utilisées par les pilotes de démarrage, si nécessaire. Ces fonctions sont requises :

-   [CmRegisterCallbackEx](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [CmUnRegisterCallback](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)

Pour plus d’informations sur la configuration requise pour le pilote ELAM et l’utilisation des API, consultez [lancement anticipé d’un logiciel anti-programme malveillant](/windows-hardware/drivers/install/early-launch-antimalware).

## <a name="tests"></a>Tests

Les pilotes ELAM doivent être spécialement signés par Microsoft pour s’assurer qu’ils sont démarrés par le noyau Windows au début du processus de démarrage. Pour obtenir la signature, les pilotes ELAM doivent transmettre un ensemble de tests de certification pour vérifier les performances et d’autres comportements. Ces tests sont inclus dans le kit de certification matérielle Windows.

## <a name="resources"></a>Ressources

-   [Logiciel anti-programme malveillant à lancement anticipé](/windows-hardware/drivers/install/early-launch-antimalware)
-   [CmRegisterCallbackEx](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [CmUnRegisterCallback](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)
-   [IoRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [IoUnRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)
-   [Certification matérielle avec la présentation de la Conférence du kit de certification matérielle Windows](https://channel9.msdn.com/events/BUILD/BUILD2011/HW-659T)
-   [Télécharger les kits et les outils](https://msdn.microsoft.com/windows/hardware/br259105)

 

 
