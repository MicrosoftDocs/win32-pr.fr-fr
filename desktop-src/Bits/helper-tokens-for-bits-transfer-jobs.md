---
title: Jetons d’assistance pour les tâches de transfert BITS
description: Jetons d’assistance pour les tâches de transfert BITS
ms.assetid: f29f9870-e406-472b-9342-203def7453ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52925a6e0d5a9601e21848d514214bfb843f6246
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463683"
---
# <a name="helper-tokens-for-bits-transfer-jobs"></a>Jetons d’assistance pour les tâches de transfert BITS

Dans Windows Vista, le service Service de transfert intelligent en arrière-plan (BITS) permet à une application d’associer un jeton de sécurité unique à une tâche de transfert BITS. La tâche de transfert BITS utilise ensuite ce jeton pour l’authentification et l’accès aux ressources locales et distantes.

Dans Windows 7, le service BITS associe un jeton supplémentaire à une tâche de transfert BITS. La tâche de transfert BITS peut être configurée avec un jeton de sécurité supplémentaire, qui est un jeton d’emprunt d’identité créé par une application appelant l’API COM BITS. Ce modèle de jeton d’assistance permet aux applications d’utiliser simultanément deux jetons de sécurité différents pour accéder à des fichiers locaux, à des certificats côté client, à des fichiers distants et à des proxies. Par exemple, une tâche de transfert BITS est créée, qui écrit les données téléchargées dans un répertoire local privilégié, puis présente une identité de domaine à faibles privilèges pour le serveur HTTP et le serveur proxy.

Une application, généralement un service Windows, spécifie un jeton d’assistance à l’aide de la nouvelle interface [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions). Cette interface est implémentée par l’objet de traitement BITS. L’application appelle [**méthode ibackgroundcopyjob :: QueryInterface**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) pour recevoir le pointeur d’interface. L’application emprunte l’identité de l’identité de l’assistance et appelle [**IBitsTokenOptions :: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) pour transmettre le jeton au service bits. L’application spécifie ensuite les ressources auxquelles le jeton s’applique en passant un jeu d’indicateurs binaires à l’aide de [**IBitsTokenOptions :: SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags). L’application efface tous les indicateurs (à l’aide de **SetHelperTokenFlags** ) pour rétablir le comportement. Le service BITS stocke les indicateurs de bits et le jeton dans la tâche de transfert BITS.

Lorsque le propriétaire des tâches de transfert BITS se déconnecte, le service BITS ignore les jetons d’assistance associés à la tâche de transfert. Si le transfert n’est pas terminé, le service BITS place le travail dans un état d’erreur avec le code d’erreur **BG \_ E \_ Token \_ requis** et ignore le jeton d’assistance. L’application cliente peut actualiser le jeton en appelant [**IBitsTokenOptions :: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) et peut ensuite reprendre la tâche de transfert bits. L’application cliente peut également effacer les indicateurs de jeton d’assistance à l’aide de [**IBitsTokenOptions :: SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) , puis reprendre la tâche de transfert sans jeton d’assistance.

De même, lorsque le propriétaire d’une session des services Terminal Server se déconnecte, le service BITS doit supprimer tous les jetons d’assistance de cette session et placer les tâches de transfert affectées dans un état d’erreur avec le code d’erreur **BG \_ E \_ Token \_ requis** .

Le modèle de jeton d’assistance nécessite une modification de la stratégie de contrôle d’accès BITS. Les versions précédentes de BITS implémentaient des contrôles d’accès à chaque appel de méthode. À compter de Windows 7, le contrôle d’accès doit être effectué à l’intérieur de l’appel [**méthode ibackgroundcopyjob :: QueryInterface**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) ; dans le cas contraire, le jeton d’assistance peut ne pas avoir accès à la tâche de transfert.

> [!Note]  
> Les implémentations plus anciennes nécessitaient efficacement que les utilisateurs du service BITS disposent de privilèges d’administrateur pour définir des jetons d’assistance. À compter de Windows 10, version 1607, les BITS non-administrateurs peuvent utiliser [**IBitsTokenOptions :: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) pour définir des jetons d’assistance non-administrateur sur les travaux bits qu’ils possèdent. Cette modification permet aux utilisateurs non-administrateurs BITS (tels que les services de téléchargeur en arrière-plan s’exécutant sous le [compte NetworkService](/windows/desktop/Services/networkservice-account)) de définir des jetons d’assistance.
>
> Plus précisément, l’implémentation a été modifiée pour permettre aux utilisateurs dépourvus de privilèges d’administrateur de définir des jetons d’assistance, à condition que les conditions suivantes soient remplies :
>
> -   pendant l’appel de [**méthode ibackgroundcopyjob :: QueryInterface**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) , le SID du jeton thread’s de l’appelant est le même que le SID du compte d’utilisateur du propriétaire du travail, et
> -   Lorsque [**IBitsTokenOptions :: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) est appelé, le jeton d’assistance n’a pas le SID d’administrateur **( \_ \_ \_ administrateurs RID d’alias de domaine**) activé.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
</dt> </dl>

 

 