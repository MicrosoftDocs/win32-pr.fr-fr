---
description: Avec la version 2,0, les compteurs de performances ont modifié l’architecture pour simplifier le processus de fourniture des données de compteur aux consommateurs.
ms.assetid: 37f75b15-3f52-4259-a6d9-5a1a14f88379
title: Fourniture de données de compteurs à l’aide de la version 2,0
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 67976c8a0b6c77582ed8c50c2e5cf753c77fcf6b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218268"
---
# <a name="providing-counter-data-using-version-20"></a>Fourniture de données de compteurs à l’aide de la version 2,0

Les fournisseurs de données de performances modernes utilisent un manifeste pour définir les données de compteur et utiliser les API du fournisseur de compteurs de performance pour gérer les données dans le contexte du fournisseur. Les fournisseurs implémentés à l’aide d’un manifeste et des API du fournisseur de compteurs de performances sont souvent appelés **fournisseurs v2**. Windows prend en charge les fournisseurs v2 en mode utilisateur sur Windows Vista ou version ultérieure et les fournisseurs v2 en mode noyau sur Windows 7 ou version ultérieure.

Cette page décrit les fournisseurs V2 en mode utilisateur. Pour plus d’informations sur les fournisseurs V2 en mode noyau, consultez [surveillance des performances en mode noyau](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring).

Au moment de l’exécution, les fournisseurs v2 fonctionnent comme suit :

- le processus du fournisseur s’inscrit auprès du système de compteur de performances Windows en appelant PerfStartProvider et PerfSetCounterSetInfo. Le fournisseur fournit éventuellement une fonction de rappel qui est avertie des demandes des consommateurs.
- Le processus du fournisseur ajoute ou supprime des instances en fonction des besoins à l’aide de PerfCreateInstance et PerfDeleteInstance. Le fournisseur met à jour les valeurs de compteur quand elles changent à l’aide d’API PerfSet * * *.
- Un consommateur effectue une demande de données à partir d’un CounterSet. Le système vérifie que l’appelant dispose des autorisations nécessaires pour collecter les données. Le système utilise ensuite un thread de travail en cours d’exécution dans le processus du fournisseur pour gérer la demande, en appelant la fonction de rappel du fournisseur, le cas échéant. Le thread de travail copie les données collectées dans une mémoire tampon gérée par le système et le système retourne ensuite les données au consommateur.

## <a name="steps-to-creating-a-provider"></a>Étapes de création d’un fournisseur

1. Écrivez un manifeste qui définit les données de compteur que votre fournisseur fournira. Pour plus d’informations sur l’écriture du manifeste, consultez [schéma des compteurs de performances](performance-counters-schema.md).
2. Utilisez [CTRPP](ctrpp.md) pour générer le code de modèle que vous incluez dans votre fournisseur. Le code du modèle comprend les structures qui définissent les ensembles de compteurs, les fonctions [**CounterInitialize**](counterinitialize.md) et [**CounterCleanup**](countercleanup.md) , ainsi que les chaînes de ressources.

   Votre fournisseur doit appeler les fonctions [**CounterInitialize**](counterinitialize.md) et [**CounterCleanup**](countercleanup.md) . **CounterInitialize** appelle la fonction [**PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) pour inscrire le fournisseur et appelle également la fonction [**PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) pour initialiser l’ensemble de compteurs. **CounterCleanup** appelle la fonction [**PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) pour supprimer l’inscription du fournisseur.

3. Incluez le code de modèle de l’étape précédente de votre projet et complétez votre fournisseur.

   Pour terminer le fournisseur, vous devez appeler la fonction [**PerfCreateInstance**](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance) pour chaque instance de l’ensemble de compteurs que vous fournissez.

   Pour définir les valeurs de compteur, appelez l’une des fonctions suivantes :

   - [**PerfSetULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
   - [**PerfSetULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
   - [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)

   L’avantage de l’utilisation de [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue) est que vous n’avez pas à effectuer d’appel de fonction pour définir ou mettre à jour la valeur de compteur, mais simplement mettre à jour votre variable de compteur locale (la variable vers laquelle les points de référence) et les compteurs de performance utilisent le pointeur pour accéder à la valeur de compteur.

   Si vous n’utilisez pas [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue), vous pouvez utiliser les fonctions suivantes pour incrémenter ou décrémenter la valeur du compteur :

   - [**PerfDecrementULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulongcountervalue)
   - [**PerfDecrementULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulonglongcountervalue)
   - [**PerfIncrementULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue)
   - [**PerfIncrementULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulonglongcountervalue)

   Avant que le fournisseur ne s’arrête, il doit appeler [**PerfDeleteInstance**](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance) pour chaque instance d’ensemble de compteurs qu’il a créée.

   Si vous avez spécifié l’attribut de **rappel** dans l’élément de [**fournisseur**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) de votre manifeste ou si vous avez utilisé l’argument **-NotificationCallback** lors de l’appel de [CTRPP](ctrpp.md), vous devez implémenter la fonction de rappel [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) . Vous transmettez la fonction de rappel à [**CounterInitialize**](counterinitialize.md).

   Si vous avez utilisé le **-MemoryRoutines** lors de l’appel de [CTRPP](ctrpp.md), vous devez implémenter les fonctions de rappel [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) et [*FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) . Vous transmettez les fonctions de rappel à [**CounterInitialize**](counterinitialize.md).

4. Lors de l’installation de votre fournisseur, utilisez l’outil LodCtr pour écrire le nom du fichier binaire qui contient les chaînes de ressources localisées et les ID de ressource dans le registre. Pour plus d’informations sur l’utilisation de LodCtr, consultez [schéma des compteurs de performances](performance-counters-schema.md).

5. Lors de la désinstallation de votre fournisseur, utilisez l’outil UnlodCtr pour supprimer les informations de votre fournisseur du Registre.
