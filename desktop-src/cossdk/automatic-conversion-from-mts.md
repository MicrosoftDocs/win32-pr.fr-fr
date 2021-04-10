---
description: Conversion automatique à partir de MTS
ms.assetid: 0848639a-26ce-47ad-8384-8969a7c3bcde
title: Conversion automatique à partir de MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d424a443995c9fff9073878a43543d4c029a2445
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111050"
---
# <a name="automatic-conversion-from-mts"></a>Conversion automatique à partir de MTS

La conversion automatique se produit en deux étapes, comme suit :

1.  Pendant l’installation de Windows. La conversion est gérée par le processus d’installation de Windows via l’utilitaire MTSTOCOM.
    > [!Note]  
    > Si l’étape 1 échoue, une partie ou la totalité des packages MTS peut avoir été convertie, mais certaines propriétés peuvent être manquantes. Dans ce cas, utilisez l’outil d’administration Services de composants pour vérifier tous les attributs. Les attributs MTS sont toujours présents sur l’ordinateur (dans le registre système de HKEY \_ local \_ machine \\ Microsoft \\ Transaction Server), mais ils sont accessibles uniquement par le biais de l’utilitaire regedit.exe.

     

2.  Après le dernier redémarrage, avant l’affichage de la boîte de dialogue ouverture de session Windows. L’étape 2 gère ces actions de conversion qui requièrent l’accès au réseau (principalement la création de membres de rôle).
    > [!Note]  
    > Si l’étape 2 échoue (en raison de défaillances temporaires du réseau ou du contrôleur de domaine), il est possible de réexécuter l’utilitaire de conversion MTSTOCOM un nombre quelconque de fois. Pour ce faire, à l’invite de commandes ou après avoir sélectionné **exécuter** dans le menu **Démarrer** , tapez la commande suivante : **% windir% \\ system32 \\mtstocom.exe**.

     

## <a name="mtstocom-log-file"></a>Fichier journal MTSTOCOM

L’utilitaire MTSTOCOM génère un fichier journal (MTSTOCOM. log) dans le répertoire Windows. Ce fichier journal conserve un enregistrement de la conversion des packages MTS en applications COM+. Si des erreurs se sont produites pendant le processus de conversion, il est toujours judicieux de consulter le fichier journal pour plus d’informations. Le fichier journal intercepte les problèmes courants, tels qu’un utilisateur ou un mot de passe non valide.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résultats et problèmes de conversion COM+](com--conversion-results-and-issues.md)
</dt> <dt>

[Conversion manuelle à partir de MTS](manual-conversion-from-mts.md)
</dt> <dt>

[Bibliothèque d’administration MTS](mts-administration-library.md)
</dt> </dl>

 

 



