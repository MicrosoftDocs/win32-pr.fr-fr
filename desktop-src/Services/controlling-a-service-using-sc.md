---
description: l’SDK Windows contient un utilitaire de ligne de commande, Sc.exe, qui peut être utilisé pour contrôler un service. Ses commandes correspondent aux fonctions fournies par le SCM. La syntaxe est la suivante.
ms.assetid: 7c3e5c39-ec0f-4174-9ecf-239927de3d39
title: Contrôle d’un service à l’aide de SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2481e0d13f19760c042d39efe4ec6094a3ef270312aeb31d2228d401d914bc1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126449"
---
# <a name="controlling-a-service-using-sc"></a>Contrôle d’un service à l’aide de SC

l’SDK Windows contient un utilitaire de ligne de commande, Sc.exe, qui peut être utilisé pour contrôler un service. Ses commandes correspondent aux fonctions fournies par le SCM. La syntaxe est la suivante.

## <a name="syntax"></a>Syntaxe

**SC** \[ *Nom du serveur* \] *Commande* \[  \] ServiceName \[  \] option1 \[ *option2* \] ...

<dl> <dt>

<span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*Nom du serveur*
</dt> <dd>

Nom de serveur facultatif. Utilisez le formulaire \\ \\ *ServerName*.

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Commande*
</dt> <dd>

L’une des commandes suivantes :

<dl> <dd>continue</dd> <dd>contrôle</dd> <dd>interroger</dd> <dd>pause</dd> <dd>start</dd> <dd>stop</dd> </dl> </dd> <dt>

<span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*FormName*
</dt> <dd>

Nom du service, tel qu’il a été spécifié lors de son installation.

</dd> <dt>

<span id="option1"></span><span id="OPTION1"></span>*option 1*
</dt> <dd>

Paramètre optionnel.

</dd> <dt>

<span id="option2"></span><span id="OPTION2"></span>*option2*
</dt> <dd>

Paramètre optionnel.

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour afficher la syntaxe complète d’une commande, utilisez la commande suivante :

 *commande* SC

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Demandes de contrôle de service](service-control-requests.md)
</dt> <dt>

[Démarrage du service](service-startup.md)
</dt> </dl>

 

 



