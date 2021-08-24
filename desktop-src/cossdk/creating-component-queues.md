---
description: Une application qui contient au moins un composant peut être marquée comme en file d’attente à l’aide de l’outil d’administration Services de composants.
ms.assetid: 7d9fec63-0bb7-45f3-9d40-736a60d69185
title: Création de files d’attente de composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c44f670cea15e1cb1a4549d5c1e847956eb41d400ae01d557803dbd1ce2b439
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793459"
---
# <a name="creating-component-queues"></a>Création de files d’attente de composants

Une application qui contient au moins un composant peut être marquée comme en file d’attente à l’aide de l’outil d’administration Services de composants.

Lorsqu’une application est marquée comme en file d’attente, COM+ crée automatiquement une file d’attente Message Queuing. Le nom de la file d’attente est le nom de l’application ; Si le nom de la file d’attente correspond au nom d’une file d’attente existante, COM+ utilise la file d’attente existante.

> [!Note]  
> Le paramètre Message Queuing *pathname* est une combinaison du nom de serveur distant (RSN) et du nom de l’application com+. Le RSN fait référence à la cible d’une activation à distance. Vous spécifiez un RSN lors de l’installation d’une application cliente exportable sur un ordinateur client. La procédure d’installation utilise le RSN pour diriger l’activation vers un ordinateur client spécifié. Pour plus d’informations sur les noms de files d’attente, reportez-vous à la table de paramètres dans la section « paramètres de moniker de la file d’attente » dans [utilisation du moniker de la file d’attente](using-the-queue-moniker.md).

 

## <a name="component-services-administrative-tool"></a>Outil d’administration Services de composants

Pour spécifier une application COM+ en file d’attente, procédez comme suit :

1.  Dans l’arborescence de la console de l’outil d’administration Services de composants, sous **services de composants**, ouvrez le dossier **applications com+** associé à l’ordinateur que vous souhaitez gérer.

2.  Cliquez avec le bouton droit sur l’application pour laquelle vous souhaitez créer une file d’attente, puis cliquez sur **Propriétés**.

3.  Sélectionnez l’onglet mise en **file d’attente** dans la boîte de dialogue Propriétés.

4.  Activez la case à cocher **en attente : cette application est accessible par les files d’attente MSMQ**.

    > [!Note]  
    > Si la case à cocher en attente est grisée, l’application ne contient aucun composant de la mise en **file d’attente** .

     

5.  Cliquez sur **OK**.

## <a name="visual-basic"></a>Visual Basic

Non applicable.

## <a name="cc"></a>C/C++

Non applicable.

## <a name="remarks"></a>Remarques

Les files d’attente créées par la bibliothèque d’administration COM+ ou l’outil d’administration Services de composants sont marquées avec l’attribut transactionnel Message Queuing.

Une fois qu’une application en file d’attente est installée sur le serveur, elle peut être mise à la disposition des clients en exportant l’application, puis en important l’application sur chaque client.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de composants de mise en file d’attente](creating-queuable-components.md)
</dt> <dt>

[Architecture des composants en file d’attente](queued-components-architecture.md)
</dt> </dl>

 

 



