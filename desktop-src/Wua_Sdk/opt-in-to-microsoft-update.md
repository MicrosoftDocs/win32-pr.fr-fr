---
description: Vous pouvez choisir un ordinateur dans le service Microsoft Update, puis inscrire ce service auprès de Mises à jour automatiques.
ms.assetid: d6f3d8ca-3b7e-409c-87b6-db247b7b68e4
title: Opt-In à Microsoft Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d034f0b224d8170a52ce359589693c601cb9598d716e9663493e8ac99edf2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994276"
---
# <a name="opt-in-to-microsoft-update"></a>Opt-In à Microsoft Update

Vous pouvez choisir un ordinateur dans le service Microsoft Update, puis inscrire ce service auprès de Mises à jour automatiques.

l’exemple de script de cette rubrique montre comment utiliser Windows Update Agent (WUA) pour inscrire le service Microsoft Update avec Mises à jour automatiques. Sinon, pour inscrire le service, l’utilisateur peut visiter Microsoft Update.

Avant de tenter d’exécuter cet exemple, vérifiez que la version de WUA installée sur l’ordinateur est la version 7.0.6000 ou une version ultérieure. Pour plus d’informations sur la façon de déterminer la version de WUA installée, consultez [détermination de la version actuelle de WUA](determining-the-current-version-of-wua.md).

## <a name="example"></a>Exemple

l’exemple de script suivant montre comment utiliser l’Agent de Windows Update (WUA) pour inscrire le service Microsoft Update avec Mises à jour automatiques. L’exemple autorise le traitement différé ou hors connexion si nécessaire.

> [!IMPORTANT]
> ce script est destiné à illustrer l’utilisation des api d’Agent Windows Update et fournit un exemple de la façon dont les développeurs peuvent utiliser ces api pour résoudre les problèmes. ce script n’est pas conçu comme un code de production, et le script lui-même n’est pas pris en charge par Microsoft (bien que les api de l’Agent de Windows Update sous-jacent soient prises en charge).

 


```VB
Set ServiceManager = CreateObject("Microsoft.Update.ServiceManager")
ServiceManager.ClientApplicationID = "My App"

'add the Microsoft Update Service, GUID
Set NewUpdateService = ServiceManager.AddService2("7971f918-a847-4430-9279-4a52d1efe18d",7,"")

```



Dans les versions antérieures de WUA (version WUA minimale de 7.0.6000), vous pouvez simplifier le processus d’abonnement à l’aide d’un paramètre du Registre. Une fois la clé de Registre et les valeurs configurées, le Microsoft Update processus d’abonnement se produit la prochaine fois que WUA effectue une recherche. Le processus d’abonnement peut être déclenché par Mises à jour automatiques ou par un appelant d’API.

Par exemple, le chemin d’accès complet de la clé de Registre et les valeurs à définir pour le processus d’abonnement sont les suivants :

**HKLM** \\ **Logiciel** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Windowsupdate** \\ **PendingServiceRegistration** \\ **7971f918-A847-4430-9279-4a52d1efe18d**

**ClientApplicationID** = mon application

**RegisterWithAU** = 1

> [!Note]
>
> La clé de Registre est respectée une seule fois lorsque WUA est mis à jour à partir d’une version antérieure à la version 7.0.6000 vers la version 7.0.6000 ou vers une version ultérieure. Nous vous recommandons d’utiliser le remplacement des valeurs de Registre existantes, car le remplacement des valeurs peut modifier le résultat d’une demande d’inscription de service antérieure.
>
> La création de cette clé de Registre nécessite des informations d’identification d’administration. pour Windows Vista, l’appelant doit créer la clé de registre dans un processus avec élévation de privilèges.

 

 

 



