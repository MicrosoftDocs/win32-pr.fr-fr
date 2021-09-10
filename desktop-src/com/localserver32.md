---
title: LocalServer32
description: Spécifie le chemin d’accès complet à une application serveur locale 32 bits.
ms.assetid: 5d922230-f53d-4bf9-be50-c8c00f45b7a8
keywords:
- Clé de registre LocalServer32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd068f51f33b6c283384198c0206bc9c3b6357f
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363327"
---
# <a name="localserver32"></a>LocalServer32

Spécifie le chemin d’accès complet à une application serveur locale 32 bits.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      LocalServer32
         (Default) = path
         ServerExecutable = path
```

## <a name="remarks"></a>Remarques

la valeur **ServerExecutable** , qui est de type **REG \_ SZ** et est prise en charge à partir de Windows Server 2003, fonctionne conjointement avec la sous-clé **LocalServer32** pour éviter toute ambiguïté lors de l’utilisation de la fonction [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) . **LocalServer32** spécifie l’emplacement de l’application de serveur com à lancer, et ces informations sont transmises en tant que premier paramètre *lpApplicationName* pour **CreateProcess**. Selon l’implémentation de **CreateProcess**, ces informations peuvent être ambiguës. Pour cette raison, si **ServerExecutable** est spécifié, com transmet la valeur nommée **ServerExecutable** au paramètre *lpApplicationName* de **CreateProcess**. Si **ServerExecutable** n’est pas spécifié, com transmet **null** comme valeur pour le premier paramètre de **CreateProcess**.

Pour garantir la sécurité du système, utilisez des chaînes entre guillemets dans le chemin d’accès pour indiquer l’emplacement où le nom de fichier exécutable se termine et les arguments commencent. Par exemple, au lieu de spécifier le chemin d’accès suivant comme entrée **LocalServer32** :

« C : \\ Program Files \\ fichiers de la société \\Application.exe param1 param2 »

Spécifiez le chemin d’accès à l’aide de la syntaxe suivante :

" \\ " C : \\ Program Files \\ fichiers de la société \\Application.exe\\ "param1 param2"

COM ajoute l’indicateur « -Embedding » à la chaîne, de sorte que l’application qui utilise les indicateurs doit analyser l’intégralité de la chaîne et vérifier l’indicateur d’incorporation.

Lorsque COM démarre un serveur local 32 bits, le serveur doit inscrire un objet de classe dans un délai écoulé défini par l’utilisateur. Par défaut, la valeur du temps écoulé doit être d’au moins 5 minutes, en millisecondes, mais ne peut pas dépasser le nombre de millisecondes dans 30 jours. En général, les applications ne doivent pas définir cette valeur, qui se trouve dans l’entrée HKEY de l' **\_ ordinateur local de l' \_ ordinateur \\ \\ Microsoft \\ COM2 \\ ServerStartElapsedTime** .

Les entrées requises pour les serveurs locaux 32 bits sont [**InprocHandler32**](inprochandler32.md), [**LocalServer**](localserver.md), **LocalServer32** et [**Insertable**](insertable.md).

Si un conteneur recherche un serveur local dans le registre, un serveur local 32 bits est prioritaire sur un serveur local de 16 bits.

Si vous implémentez des classes en tant que services, vous devez savoir que la valeur nommée [**LocalService**](localservice.md) est utilisée de préférence à la clé **LocalServer32** pour l’activation locale et distante requestsâ» si **LocalService** existe et qu’il fait référence à un service valide, la clé **LocalServer32** est ignorée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**LocalServer**](localserver.md)
</dt> <dt>

[**LocalService**](localservice.md)
</dt> </dl>

 

 