---
description: L’SDK Windows contient un utilitaire de ligne de commande, Sc.exe, qui peut être utilisé pour interroger ou modifier la base de données de services installés. Ses commandes correspondent aux fonctions fournies par le SCM. La syntaxe est la suivante.
ms.assetid: d304922c-86fb-4c62-9bfa-c827df4aecd8
title: Configuration d’un service à l’aide de SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f65669a3a7daa7e0d02731e6423adfbb3806f11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514801"
---
# <a name="configuring-a-service-using-sc"></a>Configuration d’un service à l’aide de SC

L’SDK Windows contient un utilitaire de ligne de commande, Sc.exe, qui peut être utilisé pour interroger ou modifier la base de données de services installés. Ses commandes correspondent aux fonctions fournies par le SCM. La syntaxe est la suivante.

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

<dl> <dd>boot</dd> <dd>config</dd> <dd>create</dd> <dd>supprimer</dd> <dd>description</dd> <dd>EnumDepend</dd> <dd>échec</dd> <dd>failureflag</dd> <dd>GetDisplayName,</dd> <dd>GetKeyName</dd> <dd>Verrouillage</dd> <dd>qc</dd> <dd>qdescription</dd> <dd>qfailure</dd> <dd>qfailureflag</dd> <dd>qprivs</dd> <dd>qsidtype</dd> <dd>query</dd> <dd>QueryEx</dd> <dd>privilèges</dd> <dd>QueryLock</dd> <dd>sdset</dd> <dd>sdshow</dd> <dd>showsid</dd> <dd>sidtype</dd> </dl> </dd> <dt>

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

## <a name="remarks"></a>Notes

Pour afficher la syntaxe complète d’une commande, utilisez la commande suivante :

 *commande* SC

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration de service](service-configuration.md)
</dt> <dt>

[Installation, suppression et énumération des services](service-installation-removal-and-enumeration.md)
</dt> </dl>

 

 



