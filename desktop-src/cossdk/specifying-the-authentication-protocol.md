---
description: Spécification du protocole d’authentification
ms.assetid: 2f469332-6b3e-475a-9ec6-782e1e445672
title: Spécification du protocole d’authentification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86c4688894543a45f49c4af470658da97e30a159c47025398ac7c7ae5e0620e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610509"
---
# <a name="specifying-the-authentication-protocol"></a>Spécification du protocole d’authentification

En fonction des exigences de sécurité de votre site, vous pouvez exiger que le service des composants en file d’attente vérifie toujours l’identité d’un client, ne jamais vérifier l’identité d’un client, ou pour vérifier l’identité d’un client uniquement si le composant est configuré pour exiger une authentification même lorsqu’il n’est pas accessible par le biais d’une file d’attente.

> [!Note]  
> Pour pouvoir utiliser un composant mis en file d’attente en mode groupe de travail, le niveau d’authentification doit être défini sur aucun.

 

## <a name="component-services-administrative-tool"></a>Outil d’administration Services de composants

Pour spécifier le protocole d’authentification, procédez comme suit :

1.  Dans l’arborescence de la console de l’outil d’administration Services de composants, sous **services de composants**, ouvrez le dossier **applications com+** associé à l’ordinateur que vous souhaitez gérer.

2.  Cliquez avec le bouton droit sur l’application en file d’attente pour laquelle vous souhaitez spécifier le protocole d’authentification, puis cliquez sur **Propriétés**.

3.  Sélectionnez l’onglet mise en **file d’attente** dans la boîte de dialogue Propriétés.

4.  Sous **authentification des messages MSMQ**, sélectionnez la case d’option associée au protocole d’authentification que vous souhaitez implémenter.

5.  Cliquez sur **OK**.

## <a name="visual-basic"></a>Visual Basic

Utilisez le paramètre *AuthLevel* lors de l’activation de l’application en file d’attente comme décrit dans la section [utilisation du moniker de la file d’attente](using-the-queue-moniker.md).

## <a name="cc"></a>C/C++

Utilisez le paramètre *AuthLevel* lors de l’activation de l’application en file d’attente comme décrit dans la section [utilisation du moniker de la file d’attente](using-the-queue-moniker.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sécurité des composants en file d’attente](queued-components-security.md)
</dt> <dt>

[Limitations de sécurité en mode groupe de travail](security-limitations-in-workgroup-mode.md)
</dt> </dl>

 

 



