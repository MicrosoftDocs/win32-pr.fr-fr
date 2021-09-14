---
description: Gestion des descripteurs de fichiers transactionnels dans NTFS transactionnel.
ms.assetid: 29879a3f-14b4-462c-a001-46c3c3eb74d1
title: Utilisation de NTFS transactionnel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43681f0d5b27f0db03d8b6c44564b792fce4b467
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009928"
---
# <a name="how-to-use-transactional-ntfs"></a>Utilisation de NTFS transactionnel

## <a name="transacted-file-handles"></a>Handles de fichiers traités

NTFS transactionnel (TxF) lie un descripteur de fichier à une transaction. Pour les opérations qui fonctionnent sur un descripteur (par exemple, les fonctions [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) et [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) ), l’appel de la fonction d’API réel ne change pas. Pour les opérations de fichier qui prennent un nom, il existe des fonctions transactionnelles explicites pour ces opérations. Par exemple, au lieu d’appeler [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea), appelez [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda). Cela crée un descripteur de fichier transactionnel, qui peut ensuite être utilisé pour toutes les opérations de fichier nécessitant un descripteur. Toutes les opérations suivantes utilisant ce handle sont des opérations traitées.

## <a name="basic-txf-usage"></a>Utilisation de base de TxF

La série d’étapes suivante représente l’utilisation la plus basique de TxF. Des scénarios plus complexes sont également pris en charge, à la discrétion du concepteur d’application.

1.  Créez une transaction en appelant la fonction KTM [**CreateTransaction**](/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction) ou à l’aide de l’interface **IKernelTransaction** de l' [Distributed Transaction Coordinator](/previous-versions/windows/desktop/mscs/distributed-transaction-coordinator) (DTC).
2.  Récupérez le ou les descripteurs de fichiers traités en appelant [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda).
3.  Modifiez le ou les fichiers en fonction des besoins à l’aide du ou des descripteurs de fichiers traités.
4.  Fermez tous les descripteurs de fichiers traités associés à la transaction créée à l’étape 1.
5.  Validez ou annulez la transaction en appelant la fonction KTM ou DTC correspondante.

## <a name="key-points-of-the-txf-programming-model"></a>Points clés du modèle de programmation TxF

Le modèle de programmation TxF contient les points clés suivants que vous devez prendre en compte lorsque vous développez une application TxF :

-   Il est fortement recommandé qu’une application ferme tous les descripteurs de fichiers transactionnels avant de valider ou de restaurer une transaction. Le système invalide tous les descripteurs traités lorsqu’une transaction se termine. Toute opération, à l’exception de Close, effectuée sur un handle traité après la fin de la transaction retourne l’erreur suivante : le **handle d’erreur \_ \_ n' \_ est plus \_ valide**.
-   Un fichier est affiché en tant qu’unité de stockage. Les mises à jour partielles et les remplacements de fichiers complets sont pris en charge. Plusieurs transactions ne peuvent pas modifier simultanément le même fichier.
-   Les e/s mappées en mémoire sont transparentes et cohérentes avec les e/s de fichier normales. Une application doit vider et fermer une section ouverte avant de valider une transaction. Si vous ne le faites pas, vous risquez d’avoir des modifications partielles apportées au fichier mappé au sein de la transaction. Une restauration échoue si cela n’est pas effectué.

## <a name="common-programming-errors"></a>Erreurs de programmation courantes

Les erreurs courantes suivantes peuvent se produire lors du développement d’applications transactionnelles :

-   Utilisation d’un descripteur de fichier après la fin d’une transaction.
-   Échec de la fermeture des handles aux fichiers et répertoires supprimés avant la validation d’une transaction, ce qui empêchera les opérations de suppression de se produire. Cet événement doit se produire avant d’effectuer la validation pour que l’opération de suppression soit considérée comme faisant partie de la transaction. cela est dû au fait que le système ne supprime pas réellement un fichier tant que le dernier descripteur n’est pas fermé, même lorsque l’opération n’est pas traitée, dans le cadre du sous-système d’e/s de fichier Windows.
-   Impossible de tenir compte des restaurations de transactions initiées par le système, qui peuvent se produire à tout moment ; par exemple, une transaction est restaurée si les ressources système sont épuisées.

 

 
