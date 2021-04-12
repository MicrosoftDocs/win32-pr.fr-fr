---
description: Configuration des broches de sortie demux
ms.assetid: c53f3fe6-5588-4faf-ba5c-6a6cf7e16f3a
title: Configuration des broches de sortie demux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56a24af3f49f26efe4ff6afad075a3cef61fcd1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109415"
---
# <a name="configuring-the-demux-output-pins"></a>Configuration des broches de sortie demux

Lorsque le demux MPEG-2 reçoit un paquet de données, il doit déterminer quelle broche de sortie doit analyser et remettre les données. En mode de flux de programme, le demux mappe des ID de flux à des broches de sortie. En mode de flux de transport, il mappe les PID aux broches de sortie. Par exemple, en mode de flux de transport, si PID 0x31 est mappé à la broche 0, chaque paquet TS avec ce numéro PID est routé vers la broche de sortie 0. Si le demux reçoit un paquet dont l’ID de flux ou le PID n’est mappé à aucune broche de sortie, il ignore simplement le paquet.

En mode par extraction, le demux crée automatiquement des broches de sortie pour les flux audio et vidéo dans le fichier, et mappe les ID de flux aux broches.

En mode push, les broches de sortie doivent être configurées par l’application ou par un autre filtre. Pour les sources de télévision numérique utilisant l’architecture de pilote de diffusion (BDA), le filtre de fournisseur de réseau fonctionne avec le filtre TIF pour configurer demux. L’application n’a rien à faire. Dans d’autres scénarios, l’application doit configurer les broches de sortie.

Le demux démarre sans broches de sortie. Pour créer une broche de sortie, appelez la méthode [**IMpeg2Demultiplexer :: CreateOutputPin**](/windows/desktop/api/Strmif/nf-strmif-impeg2demultiplexer-createoutputpin) sur le filtre. Cette méthode prend un type de média et un nom de code confidentiel, et retourne un pointeur **IPIN** . Le type de média est utilisé lorsque le code confidentiel se connecte à un autre filtre, en général un décodeur. un exemple est donné à la section [utilisation de demux avec des flux élémentaires](using-the-demux-with-elementary-streams.md). Le nom du code confidentiel peut être tout ce que vous aimez, sauf que les noms de code confidentiel en double ne sont pas autorisés.

Ensuite, attribuez un ou plusieurs ID de flux ou PID à la nouvelle broche de sortie. Pour les flux de programme, interrogez le code PIN pour **IMPEG2StreamIdMap** et appelez [**IMPEG2StreamIdMap :: MapStreamId**](/windows/desktop/api/Strmif/nf-strmif-impeg2streamidmap-mapstreamid). Pour les flux de transport, interrogez le code PIN pour **IMPEG2PIDMap** et appelez [**IMPEG2PIDMap :: MapPID**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid).

Le demux peut analyser des paquets TS de plusieurs façons. Pour chaque broche de sortie, la méthode d’analyse est déterminée par le paramètre *MediaSampleContent* de la méthode **MapPID** .



| Valeur                     | Description                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_flux élémentaire du média \_ | Le filtre remet les charges utiles PES. Dans ce mode, le filtre depacketizes les paquets PES, de sorte que le filtre en aval reçoit le flux ES octets, sans les en-têtes de paquets PES. (Flux audio et vidéo uniquement.)                                                                                                                                                     |
| MEDIA \_ MPEG2 \_ psi         | Le filtre fournit des sections PSI complètes, telles que les tables PAT, les tables VPM, les tables CAT, etc.                                                                                                                                                                                                                                                               |
| \_charge utile de transport multimédia \_ | Le filtre extrait les charges utiles des paquets TS et les remet sans analyse supplémentaire. Pour les flux élémentaires, cela signifie que le demux fournira des paquets PES complets, y compris les en-têtes de paquets PES.                                                                                                                                                    |
| \_paquet de transport multimédia \_  | Le filtre fournit des paquets TS complets. Le demux route les paquets TS en fonction de leurs PID, mais n’examine pas et ne traite pas les paquets. Les paquets comportant des erreurs ne sont pas filtrés. Le demux ne remultiplexe pas les paquets, et le flux de sortie obtenu n’est pas un flux de transport MPEG-2 conforme. Ce mode est appelé mode *passe* . |



 

Pour les flux de programme, le demux fournit toujours des charges utiles PES.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du démultiplexeur MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



