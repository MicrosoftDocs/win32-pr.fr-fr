---
title: DefaultAccessPermission
description: Définit la liste de Access Control (ACL) des principaux qui peuvent accéder aux classes pour lesquelles il n’existe aucun paramètre AccessPermission.
ms.assetid: 02675d0e-a96c-476e-820e-e6ff3c2d1be1
keywords:
- Valeur de Registre DefaultAccessPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e6c132096807b8c234259071758ebd361421f8f
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363387"
---
# <a name="defaultaccesspermission"></a>DefaultAccessPermission

Définit la liste de Access Control (ACL) des principaux qui peuvent accéder aux classes pour lesquelles il n’existe aucun paramètre [**AccessPermission**](accesspermission.md) . Cette liste de contrôle d’accès est utilisée uniquement par les applications qui n’appellent pas [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) et qui n’ont pas de valeur **AccessPermission** sous leur clé [**AppID**](appid-key.md) .

> [!Caution]  
> Il n’est pas recommandé de modifier cette valeur, car cela affecte toutes les applications serveur COM qui ne définissent pas leur propre sécurité au niveau du processus, et peut les empêcher de fonctionner correctement. Si vous modifiez cette valeur pour affecter les paramètres de sécurité d’une application COM particulière, vous devez à la place modifier les paramètres de sécurité à l’ensemble du processus pour cette application COM particulière. Pour plus d’informations sur la définition de la sécurité au niveau du processus, consultez Définition de la [sécurité au niveau du processus](setting-processwide-security.md).

 

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultAccessPermission = ACL
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur **\_ binaire de Reg** .

Le runtime COM du serveur vérifie la liste de contrôle d’accès décrite par cette valeur tout en usurpant l’identité de l’appelant qui tente de se connecter à l’objet, et son succès détermine si l’accès est autorisé ou non. Si la vérification de l’accès échoue, la connexion à l’objet n’est pas autorisée. Si cette valeur nommée n’existe pas, seul le principal du serveur et le système local sont autorisés à appeler le serveur.

Par défaut, cette valeur ne contient aucune entrée. Seul le principal du serveur et le système sont autorisés à appeler le serveur.

Cette valeur fournit un niveau simple d’administration centralisée de l’accès à la connexion par défaut aux objets en cours d’exécution sur un ordinateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**AccessPermission**](accesspermission.md)
</dt> <dt>

[Inscription des serveurs COM](registering-com-servers.md)
</dt> <dt>

[Définition de la sécurité au niveau du processus](setting-processwide-security.md)
</dt> </dl>

 

 




