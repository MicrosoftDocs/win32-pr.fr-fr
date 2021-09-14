---
description: Cette rubrique décrit comment créer un expert générique fourni avec le kit de développement logiciel (SDK) Moniteur réseau.
ms.assetid: c05b261d-3fac-40bf-b4ff-bd766f8d148f
title: Création d’un expert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ead0ff222b72c66bfc88ec477d1a8d6a941273
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011569"
---
# <a name="building-an-expert"></a>Création d’un expert

Cette rubrique décrit comment créer un expert générique fourni avec le kit de développement logiciel (SDK) Moniteur réseau.

> [!Note]  
> Avant de créer les exemples de code suivants, installez le kit de développement logiciel (SDK) Moniteur réseau et initialisez le fichier MySetEnv.bat.

 

**Pour créer un expert générique**

1.  Ouvrez une invite de commandes Moniteur réseau et accédez au \\ sous-répertoire experts, par exemple C : \\ Program Files \\ NetMonSDK2 \\ experts.
2.  Tapez **xcopy/e/s/V Blrplate MyExpert**; Ensuite, lorsque vous y êtes invité, tapez **D**.
3.  Accédez au \\ sous-répertoire MyExpert.
4.  Tapez **ren Blrplate \* . \* MyExpert \* . \***. Assurez-vous que tous les fichiers sont correctement renommés. Vérifiez les noms de fichiers en comparant les fichiers dans le \\ \\ sous-répertoire Blrplate experts.
5.  Modifiez le Makefile en remplaçant toutes les occurrences de **Blrplate** par **MyExpert**.
6.  Modifiez les deux fichiers. cpp en remplaçant toutes les occurrences de **Blrplate** par **MyExpert**. N’oubliez pas que l’identificateur de la boîte de dialogue dans config. cpp doit être en majuscules (par exemple, **MYEXPERT**).
7.  Modifiez MyExpert. h en remplaçant toutes les occurrences de **Blrplate** par **MyExpert**.
8.  Modifiez Resrc1. h en renommant **BLRPLATE** en **MYEXPERT**. (N’oubliez pas que **MYEXPERT** doit être en majuscules).
9.  Modifiez le fichier MyExpert. RC en renommant la **boîte de dialogue d’IDD \_ BLRPLATE \_ config \_** en **IDD \_ MyExpert \_ config \_ Dialog**.
10. Tapez **NMAKE** pour générer le fichier dll. Pour vérifier la build, accédez au \\ sous-répertoire objet vérifiez que le fichier existe. Pour plus d’informations, consultez Affichage des propriétés d’un [expert dll](viewing-expert-dll-properties.md).

Une fois la génération terminée, vous disposez d’une DLL d’expert que vous pouvez tester et déployer avec Moniteur réseau. Pour plus d’informations sur l’installation d’un expert, consultez [installation d’un expert sur Moniteur réseau 2,1](installing-an-expert-to-network-monitor-2-1.md). Pour plus d’informations sur le débogage d’un expert, consultez [débogage d’un expert](debugging-an-expert.md).

 

 



