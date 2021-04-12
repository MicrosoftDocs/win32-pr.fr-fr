---
title: Blocage des commandes
description: Pour préserver l’intégrité des opérations, certaines commandes du module de plateforme sécurisée ne sont pas autorisées à être exécutées par les logiciels sur la plateforme.
ms.assetid: 47402a4a-5f8d-4648-b3ea-06c95b2a1fc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8b9a302f12e7838240ee8bfeac1ea78a3884a1
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "104381738"
---
# <a name="command-blocking"></a>Blocage des commandes

Pour préserver l’intégrité des opérations, certaines commandes du module de plateforme sécurisée ne sont pas autorisées à être exécutées par les logiciels sur la plateforme. Par exemple, certaines commandes sont exécutées uniquement par le logiciel système. Lorsque le TBS bloque une commande, une erreur est renvoyée, le cas échéant. Par défaut, le TBS bloque les commandes qui peuvent avoir un impact sur la confidentialité, la sécurité et la stabilité du système. Le TBS suppose également que d’autres parties de la pile de logiciels peuvent limiter l’accès à certaines commandes aux entités autorisées.

Pour les commandes de la version 1,2 du module de plateforme sécurisée, il existe trois listes de commandes bloquées : une liste contrôlée par la stratégie de groupe, une liste contrôlée par les administrateurs locaux et une liste par défaut. Une commande TPM est bloquée si elle figure sur une liste. Toutefois, il existe des indicateurs de stratégie de groupe pour permettre au TBS d’ignorer la liste locale et la liste par défaut. Les indicateurs de stratégie de groupe peuvent être modifiés directement ou accessibles par le biais de l’éditeur d’objets stratégie de groupe.

> [!Note]  
> La liste des commandes bloquées localement n’est pas conservée après une mise à niveau du système d’exploitation. Les commandes qui sont bloquées dans la liste stratégie de groupe sont conservées.

 

Pour les commandes de la version 2,0 du module de plateforme sécurisée, la logique de blocage est inversée. elle utilise une liste de commandes autorisées. Cette logique bloquera automatiquement les commandes qui n’étaient pas connues lors de la première création de la liste. Lorsque des commandes sont ajoutées à la spécification du module de plateforme sécurisée après la livraison d’une version de Windows, ces nouvelles commandes sont automatiquement bloquées. Seule une mise à jour du Registre ajoute ces nouvelles commandes à la liste des commandes autorisées.

À compter de Windows 10 1809 (Windows Server 2019), les commandes TPM 2,0 autorisées ne peuvent plus être manipulées via les paramètres du Registre. Pour ces versions de Windows 10, les commandes TPM 2,0 autorisées sont fixes dans le pilote du module de plateforme sécurisée. Les commandes TPM 1,2 peuvent toujours être bloquées et débloquées par le biais de modifications du Registre. 

## <a name="direct-registry-access"></a>Accès direct au registre

Les indicateurs de stratégie de groupe se trouvent sous la clé de Registre **HKEY \_ local \_ machine** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **TPM** \\ **BlockedCommands**.

Pour déterminer les listes à utiliser pour bloquer les commandes TPM, deux valeurs **DWORD** sont utilisées comme indicateurs booléens :

-   "IgnoreDefaultList"

    Si SET (la valeur existe et est différent de zéro), le TBS ignore la liste par défaut des commandes bloquées.

-   "IgnoreLocalList"

    Si SET (la valeur existe et est différent de zéro), le TBS ignore la liste locale des commandes bloquées.

## <a name="group-policy-object-editor"></a>Éditeur d'objets de stratégie de groupe

**Pour accéder à l’éditeur d’objets stratégie de groupe**

1.  Cliquez sur **Start**.
2.  Cliquez sur **Exécuter**.
3.  Dans la zone **Ouvrir** , tapez **gpedit.msc**. Cliquez sur **OK**. L’éditeur d’objets de stratégie de groupe s’ouvre.
4.  Développez Configuration de l' **ordinateur**.
5.  Développez **modèles d’administration**.
6.  Développez **système**.
7.  Développez **Services module de plateforme sécurisée (TPM)**.

Les listes de commandes TPM 1.2 bloquées spécifiques peuvent être modifiées directement aux emplacements suivants.

-   Liste des stratégies de groupe :

    ```
    HKEY_LOCAL_MACHINE
       Software
          Policies
             Microsoft
                Tpm
                   BlockedCommands
                      List
    ```

-   Liste locale :

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                SharedAccess
                   Parameters
                      Tpm
                         BlockedCommands
                            List
    ```

-   Liste par défaut :

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                BlockedCommands
                   List
    ```

Sous chacune de ces clés de Registre figure une liste de valeurs de registre de type de Registre \_ sz. Chaque valeur représente une commande TPM bloquée. Chaque clé de registre a un champ « nom de la valeur » et un champ « données de valeur ». Les deux champs (« nom de la valeur » et « données de valeur ») doivent correspondre exactement à la valeur décimale du numéro de commande du module de plateforme sécurisée à bloquer.

La liste des commandes TPM 2,0 spécifiques autorisées peut être modifiée directement à l’emplacement suivant. Sous la clé de Registre figure la liste des valeurs de Registre du type de Registre \_ DWORD. Chaque valeur représente une commande TPM 2,0 autorisée. Chaque valeur de registre a un **nom** et un champ de **valeur** . Le **nom** correspond à l’ordinal de commande TPM 2,0 hexadécimal qui doit être autorisé. La **valeur est 1** si la commande est autorisée. Si l’ordinal d’une commande n’est pas présent ou a la valeur 0, la commande est bloquée.

-   Liste par défaut :

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                AllowedW8Commands
                   List
    ```

Pour Windows 8, Windows Server 2012 et versions ultérieures, les clés de Registre **BlockedCommands** et **AllowedW8Commands** déterminent respectivement les commandes TPM bloquées ou autorisées pour les comptes d’administrateur. Les comptes d’utilisateur disposent respectivement d’une liste de commandes TPM bloquées ou autorisées dans les clés de Registre **BlockedUserCommands** et **AllowedW8UserCommands** . Dans Windows 10, version 1607, de nouvelles clés de Registre ont été introduites pour les applications AppContainer : **BlockedAppContainerCommands** et **AllowedW8AppContainerCommands**.

 

 




