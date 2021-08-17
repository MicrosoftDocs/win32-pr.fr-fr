---
title: Configuration de la journalisation des erreurs de l’API du serveur HTTP
description: La journalisation des erreurs de l’API du serveur HTTP est contrôlée par trois valeurs de Registre sous une \\ clé de paramètres http.
ms.assetid: a7712159-939e-42e3-a8d8-73148c2f4f6e
keywords:
- API serveur HTTP, configuration des journaux d’erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a10479a1b2bd1ebf559213b6cd4b738f6c0b9ea63c142edcce3c10f64f877dda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950888"
---
# <a name="configuring-http-server-api-error-logging"></a>Configuration de la journalisation des erreurs de l’API du serveur HTTP

La journalisation des erreurs de l’API du serveur http est contrôlée par trois valeurs de Registre sous une \\ clé de **paramètres** http située à l’emplacement suivant :

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

> [!Note]  
> l’emplacement et la forme des valeurs de configuration peuvent changer dans les versions ultérieures du système d’exploitation Windows.

 

Un utilisateur doit disposer des privilèges administrateur/système local pour modifier les valeurs de Registre et afficher ou modifier les fichiers journaux et le dossier qui les contient.

Les informations de configuration dans les valeurs de Registre sont lues lorsque le pilote de l’API du serveur HTTP est démarré. Par conséquent, si les paramètres sont modifiés, le pilote doit être arrêté et redémarré pour lire les nouvelles valeurs. Pour ce faire, vous pouvez utiliser les commandes de console suivantes :

**net stop http**

**NET START http**

Les fichiers journaux sont nommés à l’aide de la Convention suivante :

**HTTPERR +**  pas **+. log**

Par exemple : « httperr4. log ».

Les fichiers journaux sont recyclés lorsqu’ils atteignent la taille maximale spécifiée par la valeur de Registre **ErrorLogFileTruncateSize** , et la valeur ne peut pas être inférieure à un mégaoctet (Mo).

Si la configuration de la journalisation des erreurs n’est pas valide ou si une erreur se produit lors de l’écriture dans les fichiers journaux, l’API du serveur HTTP utilise l’enregistrement des événements pour informer les administrateurs que la journalisation des erreurs n’a pas eu lieu.

Les valeurs de configuration du Registre sont décrites dans le tableau suivant.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valeur de Registre</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="EnableErrorLogging"></span><span id="enableerrorlogging"></span><span id="ENABLEERRORLOGGING"></span>EnableErrorLogging<br/></td>
<td>Valeur <strong>DWORD</strong> qui peut être définie sur <strong>true</strong> pour activer la journalisation des erreurs, ou <strong>false</strong> pour la désactiver. La valeur par défaut est <strong>true</strong>.<br/></td>
</tr>
<tr class="even">
<td><span id="ErrorLogFileTruncateSize"></span><span id="errorlogfiletruncatesize"></span><span id="ERRORLOGFILETRUNCATESIZE"></span>ErrorLogFileTruncateSize<br/></td>
<td><strong>Valeur DWORD</strong> qui spécifie la taille maximale, en octets, d’un fichier journal des erreurs. La valeur par défaut est un mégaoctet (de 1 à 1).<br/>
<blockquote>
[!Note]<br />
La valeur spécifiée ne peut pas être inférieure à la valeur par défaut.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ErrorLoggingDir"></span><span id="errorloggingdir"></span><span id="ERRORLOGGINGDIR"></span>ErrorLoggingDir<br/></td>
<td><strong>Chaîne</strong> qui spécifie le dossier sous lequel l’API du serveur http place ses fichiers de journalisation. <br/> L’API du serveur HTTP crée un sous-dossier nommé &quot; HTTPERR &quot; sous le dossier spécifié dans lequel les fichiers journaux sont placés. Ce sous-dossier et les fichiers journaux reçoivent les mêmes paramètres d’autorisation, ce qui signifie que les comptes administrateur et système local ont un accès complet, alors que les autres utilisateurs n’ont pas accès.<br/> Si aucun dossier n’est spécifié dans le registre, le dossier par défaut est le suivant :<br/> &quot;%SystemRoot%\System32\LogFiles&quot;<br/>
<blockquote>
[!Note]<br />
La valeur de chaîne ErrorLoggingDir doit être un chemin d’accès complet, mais elle peut contenir &quot; % systemroot% &quot; .
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

 

 





