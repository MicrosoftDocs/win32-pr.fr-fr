---
description: 'En savoir plus sur : exemple de service complet'
ms.assetid: a3aeea9b-09c0-4834-892a-c378b67402f4
title: Exemple de service complet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb87ebfef3f964eacee66be94a4b5291c335d0d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520087"
---
# <a name="the-complete-service-sample"></a>Exemple de service complet

Les rubriques de cette section forment un exemple complet de service :

-   [Sample.MC](sample-mc.md) (contient des messages d’erreur)
-   [SVC. cpp](svc-cpp.md) (contient le code de service)
-   [SvcConfig. cpp](svcconfig-cpp.md) (contient le code de configuration du service)
-   [SvcControl. cpp](svccontrol-cpp.md) (contient le code de contrôle du service)

## <a name="building-the-service"></a>Génération du service

La procédure suivante décrit la génération du service et l’inscription de la DLL de message d’événement.

**Pour générer le service et inscrire la DLL de message d’événement**

1.  Générez la DLL de message à partir de Sample.mc en procédant comme suit :
    1.  **sample.mc MC-U**
    2.  **RC-r exemple. RC**
    3.  **Link-dll-NOENTRY -out:sample.dll Sample. res**
2.  Générez Svc.exe, SvcConfig.exe et SvcControl.exe à partir de svc. cpp, SvcConfig. cpp et SvcControl. cpp, respectivement.
3.  Créez la clé de Registre **HKEY \_ local \_ machine \\ System System \\ CurrentControlSet \\ services \\ EventLog \\ application \\ SvcName** et ajoutez les valeurs de Registre suivantes à cette clé.

    | Valeur                              | Type       | Description                                                                                                        |
    |------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------|
    | **EventMessageFile**  =  *\_ chemin* de la dll | SZ de REG \_    | Chemin d’accès à la DLL de ressources uniquement qui contient des chaînes que le service peut écrire dans le journal des événements.               |
    | **TypesSupported** = 0x00000007    | \_valeur DWORD reg | Masque de bits qui spécifie les types d’événements pris en charge. La valeur 0x000000007 indique que tous les types sont pris en charge. |

    

     

## <a name="testing-the-service"></a>Test du service

La procédure suivante décrit comment tester le service.

**Pour tester le service**

1.  Dans le panneau de configuration, démarrez l’application **services** . (Dans les étapes suivantes, utilisez la touche F5 pour actualiser l’affichage après l’exécution d’une commande qui modifie les informations de l’application **services** .)
2.  Exécutez la commande suivante pour installer le service :

    **installation SVC**

    Le service écrit « service correctement installé » sur la console si l’opération réussit ou un message d’erreur dans le cas contraire.

    Si l’installation du service a échoué, le service s’affiche dans l’application **services** . Notez que le **nom** est défini sur « SvcName », que la **Description** et l' **État** sont vides, et que **type de démarrage** est défini sur « manuel ».

3.  Exécutez la commande suivante pour démarrer le service :

    **svccontrol démarrer SvcName**

    Si l’opération a échoué, le programme de contrôle des services écrit « démarrage du service en attente... » puis « service démarré correctement » sur la console. Dans le cas contraire, le programme écrit un message d’erreur dans la console.

    Si le service démarre correctement, l' **État** est défini sur « démarré ». Le code de la fonction [*ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) est exécuté par le SCM. Si une erreur se produit, le service écrit un message d’erreur dans le journal des événements. Ce message comprend le nom de la fonction qui a échoué et le code d’erreur qui a été retourné en cas d’échec.

4.  Exécutez la commande suivante pour mettre à jour la description du service :

    **svcconfig décrire SvcName**

    Le programme de configuration de service écrit la description de service correctement mise à jour sur la console si l’opération réussit ou un message d’erreur dans le cas contraire.

    Si la mise à jour se déroule correctement, la **Description** est définie sur « il s’agit d’une description de test ».

5.  Exécutez la commande suivante pour interroger la configuration du service :

    **svcconfig requête SvcName**

    Le programme de configuration de service écrit les informations de configuration de service dans la console si l’opération a échoué ou un message d’erreur dans le cas contraire.

6.  Exécutez la commande suivante pour modifier la DACL de service :

    **svccontrol DACL SvcName**

    Le programme de configuration de service écrit « la liste DACL du service a été mise à jour correctement » sur la console si l’opération réussit ou un message d’erreur.

7.  Exécutez la commande suivante pour désactiver le service :

    **svcconfig désactiver SvcName**

    Le programme de configuration de service écrit « service correctement désactivé » sur la console si l’opération réussit ou un message d’erreur.

    Si le service est désactivé avec succès, le **type de démarrage** est défini sur « désactivé ».

8.  Exécutez la commande suivante pour activer le service :

    **svcconfig activer SvcName**

    Le programme de configuration de service écrit « service activé avec succès » sur la console si l’opération réussit ou un message d’erreur.

    Si le service est activé avec succès, le **type de démarrage** est défini sur « manuel ».

9.  Exécutez la commande suivante pour arrêter le service :

    **svccontrol Stop SvcName**

    Si l’opération échoue, le programme de contrôle des services écrit « arrêt du service en attente... » puis « Service arrêté correctement » sur la console. Dans le cas contraire, le programme écrit un message d’erreur dans la console.

    Si le service s’arrête correctement, l' **État** est vide.

    En cas d’échec de l’arrêt du service, le programme de contrôle des services écrit un message d’erreur dans le journal des événements qui comprend le nom de la fonction qui a échoué et le code d’erreur qui a été retourné en cas d’échec.

10. Exécutez la commande suivante pour supprimer le service :

    **svcconfig supprimer SvcName**

    Le programme de configuration de service écrit « Service supprimé avec succès » sur la console si l’opération réussit ou un message d’erreur dans le cas contraire.

    Si le service est correctement supprimé, il n’est plus affiché dans l’application **services** . (Notez que si vous tentez de supprimer un service qui n’est pas arrêté, l’opération se déroule correctement, mais le **type de démarrage** est défini sur « désactivé » et l’entrée de service est supprimée lors du redémarrage du système ou lorsque le service est arrêté à l’aide du gestionnaire des tâches.)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des services](using-services.md)
</dt> </dl>

 

 
