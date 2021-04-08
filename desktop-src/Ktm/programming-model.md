---
description: Les enregistreurs d’applications peuvent apporter des modifications mineures au code source pour ajouter des opérations de Registre et de fichier transactionnelles à l’aide du gestionnaire de transactions KTM (Kernel Transaction Manager).
ms.assetid: 356c66dc-5ddd-472f-835c-2e2cb019bcfd
title: Utilisation des transactions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 255e40fb38ca4bfb24acdce717f133dbcf0c76f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865773"
---
# <a name="working-with-transactions"></a>Utilisation des transactions

Les enregistreurs d’applications peuvent apporter des modifications mineures au code source pour ajouter des opérations de Registre et de fichier transactionnelles à l’aide du gestionnaire de transactions KTM (Kernel Transaction Manager). En général, cela implique la création d’une transaction et le passage du handle à d’autres fonctions fournies par des ressources transactionnelles telles que le [NTFS transactionnel](/windows/desktop/FileIO/transactional-ntfs-portal) et le registre traité.

KTM fournit des mécanismes permettant à votre application de participer à des transactions et d’écrire votre propre gestionnaire de ressources transactionnelles. Il existe des fonctions qui vous permettent de créer, gérer et utiliser quatre classes d’objets noyau : transactions, gestionnaires de transactions, gestionnaires de ressources et inscription. Si vous utilisez simplement des transactions, vous devez uniquement travailler avec des objets de transaction et utiliser ces fonctions :

-   [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)
-   [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)
-   [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)

Ne partez jamais du principe qu’une transaction est active. Les transactions peuvent être restaurées pour de nombreuses raisons et à tout moment.

Windows expose une interface basée sur des handles aux ressources système. Pour utiliser un objet de système d’exploitation, l’application demande tout d’abord un handle à l’objet, puis utilise ce handle dans les appels de fonction suivants pour accéder ou modifier l’objet. Un descripteur peut généralement être ouvert dans différents modes ; le mode spécifié affecte la sémantique des appels de fonction suivants. Par exemple, un descripteur de fichier ouvert par un appel à [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) avec l’indicateur *dwDesiredAccess* défini sur la **\_ lecture générique** ne peut pas être utilisé dans les appels qui modifient le fichier.

Vous pouvez coordonner avec [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) ressources en mode utilisateur, telles que SQL ou MSMQ, et avec les ressources en mode noyau qui utilisent le KTM. Commencez par créer une transaction DTC ou un objet [**System. transactions**](/dotnet/api/system.transactions?view=dotnet-plat-ext-3.1) , puis appelez l’objet [**IKernelTransaction**](/previous-versions/windows/desktop/aa344210(v=vs.85)) , à partir duquel vous pouvez obtenir le handle KTM. L’objet **IKernelTransaction** crée une transaction KTM qui est subordonnée à la transaction DTC. Avec ce handle, vous pouvez créer vos objets transactionnels, mais signaler le résultat de la transaction à l’aide de DTC ou de **System. transactions**.

 

 
